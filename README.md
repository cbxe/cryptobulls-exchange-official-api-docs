# Official Documentation for the Cryptobulls Exchange APIs and Streams.
Official Announcements regarding changes, downtime, etc. to the API and Streams will be reported here: https://www.cryptobulls.exchange/api
Streams, endpoints, parameters, payloads, etc. described in the documents in this repository are considered official and supported.
The use of any other streams, endpoints, parameters, or payloads, etc. is not supported; use them at your own risk and with no guarantees.

Exchange Pair
Returns list of all the trade pairs from exchange.


URL : https://www.cryptobulls.exchange/ticker

Response Example :

<pre>{
    "btc_eth": {
        "price_change_24h": "-2.00138026",
        "price_change_7d": "-10.60186351",
        "last_price": "0.07100000",
        "lowest_ask": "0.07245000",
        "highest_bid": "0.07750000",
        "volume": {
            "btc_trade": 35.5,
            "fee_collected": 0.071
        }
    },
    "btc_ltc": {
        "price_change_24h": "-4.85431310",
        "price_change_7d": "-6.11412358",
        "last_price": "0.01489030",
        "lowest_ask": "0.01565000",
        "highest_bid": "0.01565000",
        "volume": {
            "btc_trade": 18.5080254,
            "fee_collected": 0.0370160508
        }
    }
}
</pre>

Market Data List
Returns details of single trade pair from exchange.


URL : https://www.cryptobulls.exchange/ticker/market

Note: In the URL change the market value with real (eg. btc_eth, btc_ltc, btc_mgc, btc_sil etc....)

Response Example :

<pre>{
    "price_change_24h": "-10.89108911",
    "price_change_7d": "-25.00000000",
    "last_price": "0.00000090",
    "lowest_ask": "0.00000095",
    "highest_bid": "0.00000138",
    "volume": {
        "btc_trade": 7.0832617357782,
        "fee_collected": 0.014166523471556
    }
}</pre>

Transactions
Returns details of single trade pair transactions from exchange.

URL : https://www.cryptobulls.exchange/transaction/btc_eth

Note: In the URL change the market value with real (eg. btc_eth, btc_ltc, btc_mgc, btc_sil etc....)

Response Example :

<pre>[
    {
        "id": "9384",
        "timestamp": "1529844234",
        "price": "0.07000000",
        "amount": "10.000",
        "type": "sell"
    },
    {
        "id": "9314",
        "timestamp": "1529840301",
        "price": "0.07501200",
        "amount": "100.000",
        "type": "sell"
    },
    {
        "id": "9313",
        "timestamp": "1529840280",
        "price": "0.07501200",
        "amount": "900.000",
        "type": "sell"
    },
    {
        "id": "9312",
        "timestamp": "1529840275",
        "price": "0.07501200",
        "amount": "1000.000",
        "type": "buy"
    },
    {
        "id": "9311",
        "timestamp": "1529840233",
        "price": "0.07501200",
        "amount": "321.000",
        "type": "sell"
    },
    {
        ....
        ....
        ....
        ....
        Shows last 100 executed transactions
        
 }
]</pre>
                
