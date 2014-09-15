## Market Maker

Automatically make a market on the Ripple order book

### Installation
 
    npm install --save ripple-market-maker

### Proposed Usage

    var MarketMaker = require('ripple-market-maker');
    
    var marketMaker = new MarketMaker.Bot();

    var dogeToXrp = new MarketMaker.Market({
      buy: {
        currency: 'DOG',
        issuer: 'rMpPEZcKYjYyfTyesrYWi5VV6wcy5mTxP1',
        minimum: 100
      },
      sell: {
        currency: 'XRP',
        maximum: 1000
      },
      marketPrice: function(callback) {
        // look up conversion price from some service
        getXrpPricePerDogecoin(callback)
      }
    })

    marketMaker.make(market);

