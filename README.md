Please DOWNLOAD the LATEST [CoinMarketCap Pro Api](https://www.nuget.org/packages/CoinMarketCapProApi) 

# CoinMarketCap Api v2 Client [![Build status](https://ci.appveyor.com/api/projects/status/5b1vscy74feuungw?svg=true)](https://ci.appveyor.com/project/tosunthex/coinmarketcap-api) [![Codacy Badge](https://api.codacy.com/project/badge/Grade/3f5cd54efbf149f19c25399a4dc9abc4)](https://www.codacy.com/project/tosunthex/CoinMarketCap-Api/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=tosunthex/CoinMarketCap-Api&amp;utm_campaign=Badge_Grade_Dashboard) [![NuGet](https://img.shields.io/nuget/v/CoinMarketCapApiV2Client.svg)](https://www.nuget.org/packages/CoinMarketCapApiV2Client/)[![NuGet](https://img.shields.io/nuget/dt/CoinMarketCapApiV2Client.svg)](https://www.nuget.org/packages/CoinMarketCapApiV2Client/)

CoinMarketCap API v2 client written in .Net Standart 2.0

## Installation
This Coinmarketcap v2 api wrapper library is available on [NuGet](https://www.nuget.org/packages/CoinMarketCapApiV2Client/)

Package manager
````
Install-Package CoinMarketCapApiV2Client
````
.NET CLI
````
dotnet add package CoinMarketCapApiV2Client
````
Paket CLI
````
paket add CoinMarketCapApiV2Client
````

## Basic usage
Default values<br>
StartId = 1; Limit = 100; Sort = Rank; Currency = Usd

Get all listed cryptocurrencies:
```cs
var client = new CoinMarketCapClient();
var tickers = await client.Ticker.GetTickers();
```

Get tickers by Id 10-30 with quotes in EUR:
```cs
var client = new CoinMarketCapClient();
var tickersResponse = await client.GetTickers(10, 20, Sort.Id, Currency.Eur);
```
Get tickers by Rank 1-100 with quotes in EUR:
```cs
var client = new CoinMarketCapClient();
var tickersResponse = await client.GetTickers(1, Limit.Max, Sort.Rank, Currency.Eur);
```

Get Ripple (XRP) ticker with quote in USD:
```cs
var client = new CoinMarketCapClient();
var chainlinkTicker = await client.GetTickerAsync(1975, Currency.USD);
```

Target Frameworks and Dependencies
> .NETFramework 4.5
```
Microsoft.AspNet.WebApi.SelfHost (>= 5.2.2)
Newtonsoft.Json (>= 11.0.2)
```

>.NETFramework 4.6.1
```
Microsoft.AspNet.WebApi.SelfHost (>= 5.2.2)
Newtonsoft.Json (>= 11.0.2)
```

>.NETStandard 1.3
```
NETStandard.Library (>= 1.6.1)
Newtonsoft.Json (>= 11.0.2)
```

>.NETStandard 1.5
```
NETStandard.Library (>= 1.6.1)
Newtonsoft.Json (>= 11.0.2)
```

>.NETStandard 2.0
```
Newtonsoft.Json (>= 11.0.2)
```
