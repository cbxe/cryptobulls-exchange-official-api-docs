# Official Documentation for the Cryptobulls Exchange APIs and Streams.
Official Announcements regarding changes, downtime, etc. to the API and Streams will be reported here: https://www.cryptobulls.exchange/api
Streams, endpoints, parameters, payloads, etc. described in the documents in this repository are considered official and supported.
The use of any other streams, endpoints, parameters, or payloads, etc. is not supported; use them at your own risk and with no guarantees.

<h2 class="h3 capitalize font-bold">Exchange Pair</h2>
<small>Returns list of all the trade pairs from exchange.</small>

<p><strong>URL : </strong><a href="https://www.cryptobulls.exchange/ticker" target="_blank">https://www.cryptobulls.exchange/ticker</a></p>
<p><strong>Note:</strong> In the URL change the market value with real (eg. btc_eth, btc_ltc, btc_mgc, btc_sil etc....)</p>

<p><strong>Response Example :</strong></p>

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

<h2 class="h3 capitalize font-bold">Market Data List</h2>
<small>Returns details of single trade pair from exchange.</small>
<p><strong>URL : </strong><a href="https://www.cryptobulls.exchange/ticker/btc_eth" target="_blank">https://www.cryptobulls.exchange/ticker/market</a></p>
<p><strong>Note:</strong> In the URL change the market value with real (eg. btc_eth, btc_ltc, btc_mgc, btc_sil etc....)</p>
<p><strong>Response Example :</strong></p>
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

<h2 class="h3 capitalize font-bold">Transactions</h2>
<small>Returns details of single trade pair transactions from exchange.</small>
<p><strong>URL : </strong><a href="https://www.cryptobulls.exchange/transaction/btc_eth" target="_blank">https://www.cryptobulls.exchange/transaction/btc_eth</a></p>
<p><strong>Note:</strong> In the URL change the market value with real (eg. btc_eth, btc_ltc, btc_mgc, btc_sil etc....)</p>
<p><strong>Response Example :</strong></p>

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
                
