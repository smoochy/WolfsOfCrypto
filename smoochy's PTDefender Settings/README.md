If you are using ProfitTrailer and PTMagic, these settings might support you, when you are also using [PTDefender](https://github.com/smoochy/WolfsOfCrypto/wiki/About-PTDefender). They are based on CryptGnome's PTDefender Settings (thanks for them!)

The interesting part is in ```settings.analyzer.json```, between line 371 and 522.  

Basically you only need to change line 375 and put in the name of the coins, you want to defend.  

Line 375: ```"AllowedMarkets": "ADABTC",``` <--- If you only want to defend one coin.  
Line 375: ```"AllowedMarkets": "ADABTC, ETHBTC, QTUMBTC",``` <--- If you want to defend several coins at the same time.

**Important**: If you do not want to use this SingleMarketSetting at a certain time, it must **NOT** have an empty *AllowedMarkets*, otherwise PTMagic will crash!   

Line 375: ```"AllowedMarkets": "FantasyCoinBTC",``` <--- Works  
Line 375: ```"AllowedMarkets": "",``` <--- Will make PTMagic crash!  


If you want to, take this SingleMarketSetting and incorporate them into your own PTMagic settings. Just make sure, that it is the first SingleMarketSetting! And don't forget to copy also the needed indicators from the ```_presets/Default/INDICATORS.properties``` file.
