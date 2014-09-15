## Market Maker

Automatically make a market on the Ripple order book

### Installation
 
    npm install --save market-maker

### Proposed Usage

    var marketMaker = new MarketMaker();

    var dogeToXrp = Market({
      buy: {
        currency: 'DOG',
        issuer: 'rMpPEZcKYjYyfTyesrYWi5VV6wcy5mTxP1',
        minimum: 100
      },
      sell: {
        currency: 'XRP',
        maximum: 1000
      },
      minBuy: 100,
      convert: function(callback) {
        callback(3.2);
      }
    })

    marketMaker.make(market);

