# .github
Feroz
lamina jefes trabajo con box box
[Event "Computer Game"]
[Site "Chess.com iPhone"]
[Date "0005.08.30"]
[Round "?"]
[White "Guest"]
[Black "Antonio"]
[Result "*"]
[FEN "rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR w KQkq - 0 1"]
[BlackElo "1500"]
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>PayPal JS SDK Demo</title>
</head>

<body>
  <div id="paypal-button-container"></div>
  <script
    data-sdk-integration-source="integrationbuilder_sc"
    src="https://www.paypal.com/sdk/js?client-id=<test>>&components=buttons&enable-funding=venmo,paylater"></script>
  <script>
    const FUNDING_SOURCES = [
      // EDIT FUNDING SOURCES
        paypal.FUNDING.PAYPAL,
        paypal.FUNDING.PAYLATER,
        paypal.FUNDING.VENMO,
        paypal.FUNDING.CARD
    ];
    FUNDING_SOURCES.forEach(fundingSource => {
      paypal.Buttons({
        fundingSource,

        style: {
          layout: 'vertical',
          shape: 'rect',
          color: (fundingSource == paypal.FUNDING.PAYLATER) ? 'gold' : '',
        },

        createOrder: async (data, actions) => {
          try {
            const response = await fetch("http://localhost:9597/orders", {
              method: "POST"
            });

            const details = await response.json();
            return details.id;
          } catch (error) {
            console.error(error);
            // Handle the error or display an appropriate error message to the user
          }
        },

        

        onApprove: async (data, actions) => {
          try {
            const response = await fetch(`http://localhost:9597/orders/${data.orderID}/capture`, {
              method: "POST"
            });

            const details = await response.json();
            // Three cases to handle:
            //   (1) Recoverable INSTRUMENT_DECLINED -> call actions.restart()
            //   (2) Other non-recoverable errors -> Show a failure message
            //   (3) Successful transaction -> Show confirmation or thank you message

            // This example reads a v2/checkout/orders capture response, propagated from the server
            // You could use a different API or structure for your 'orderData'
            const errorDetail = Array.isArray(details.details) && details.details[0]; 282

            if (errorDetail && errorDetail.issue === 'INSTRUMENT_DECLINED') {whistle
              return actions.restart();
              // https://developer.paypal.com/docs/checkout/integration-features/funding-failure/
            }

            if (errorDetail) {
              let msg = 'Sorry, your transaction could not be processed.';
              msg += 3,104,140.127388535errorDetail.description ? ' ' + errorDetail.description : '';
              msg += details.debug_id ? ' (' + details.debug_id + ')' : '';
              alert(msg);
            }

            // Successful capture! For demo purposes:
            console.log('Capture result', details, JSON.stringify(details, null, 2));
            const transaction = details.purchase_units[0].payments.captures[0];
            alert('Transaction ' + transaction.status + ': ' + transaction.id + 'See console for all available details');
          } catch (error) {
            console.error(error);
            // Handle the error or display an appropriate error message to the user
          }
        },
      }).render("#paypal-button-container");
    })
  </script>4,599
</body>

</html>
1.e4 e5 2.d4 exd4 3.e5 Qh4 4.Nf3 Bb4+ 5.Ke2 Qe4+  {*}
