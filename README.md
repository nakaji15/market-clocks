<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <title>Market & World Clock Dashboard - Verified Final</title>
    <style>
        /* 全体の背景：TradingViewのダークモードに最適化 */
        body { 
            background-color: #131722; 
            color: #d1d4dc; 
            margin: 0; 
            padding: 20px; 
            font-family: -apple-system, BlinkMacSystemFont, "Trebuchet MS", Roboto, Ubuntu, sans-serif;
        }
        .main-container { 
            display: flex; 
            gap: 20px; 
            max-width: 1250px;
            margin: 0 auto;
            justify-content: center;
        }
        /* 左側：MARKET INDEX パネル */
        .market-panel { 
            flex: 0 0 640px; 
        }
        /* 右側：WORLD CLOCK パネル */
        .clock-panel { 
            flex: 0 0 340px; 
            background-color: #1e222d; 
            padding: 20px; 
            border-radius: 10px;
            display: flex;
            flex-direction: column;
            gap: 10px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.5);
            align-items: center;
        }
        /* 時計アイテムのスタイル設定 */
        .clock-item {
            width: 100%;
            text-align: center;
            border-bottom: 1px solid #363c4e;
            padding-bottom: 5px;
            overflow: hidden;
        }
        .clock-item:last-child { border-bottom: none; }
        
        /* リンクの装飾（時計の都市名など） */
        .clock-item a { color: #2962ff !important; font-weight: bold !important; font-size: 14px !important; }

        h2 {
            font-size: 16px;
            text-align: center;
            margin-top: 0;
            margin-bottom: 20px;
            color: #787b86;
            letter-spacing: 1.5px;
            text-transform: uppercase;
        }
    </style>
</head>
<body>

<div class="main-container">
    <div class="market-panel">
        <h2>MARKET INDEX</h2>
        <div class="tradingview-widget-container">
            <div class="tradingview-widget-container__widget"></div>
            <script type="text/javascript" src="https://s3.tradingview.com/external-embedding/embed-widget-market-overview.js" async>
            {
              "colorTheme": "dark",
              "dateRange": "12M",
              "showChart": true,
              "locale": "ja",
              "width": 640,
              "height": 850,
              "largeChartUrl": "",
              "isTransparent": false,
              "showSymbolLogo": true,
              "showFloatingTooltip": false,
              "plotLineColorGrowing": "rgba(242, 54, 69, 1)",
              "plotLineColorFalling": "rgba(56, 142, 60, 1)",
              "gridLineColor": "rgba(156, 156, 156, 0)",
              "scaleFontColor": "#DBDBDB",
              "belowLineFillColorGrowing": "rgba(41, 98, 255, 0.12)",
              "belowLineFillColorFalling": "rgba(41, 98, 255, 0.12)",
              "belowLineFillColorGrowingBottom": "rgba(41, 98, 255, 0)",
              "belowLineFillColorFallingBottom": "rgba(41, 98, 255, 0)",
              "symbolActiveColor": "rgba(41, 98, 255, 0.12)",
              "tabs": [
                {
                  "title": "watchlist",
                  "symbols": [
                    { "s": "INDEX:NKY", "d": "日経225" },
                    { "s": "IG:TOPIX", "d": "TOPIX" },
                    { "s": "CAPITALCOM:US500", "d": "S＆P 500" },
                    { "s": "CAPITALCOM:US100", "d": "ナスダック" },
                    { "s": "CAPITALCOM:US30", "d": "NYダウ" },
                    { "s": "FX:USDJPY", "d": "米ドル／円" },
                    { "s": "TICKMILL:EURJPY", "d": "ユーロ／円" },
                    { "s": "FX_IDC:AEDJPY", "d": "UEAディルハム／円" },
                    { "s": "BITFLYER:BTCJPY", "d": "ビットコイン／円" },
                    { "s": "PYTH:XAUUSD", "d": "金" },
                    { "s": "BLACKBULL:WTI", "d": "原油" }
                  ]
                }
              ]
            }
            </script>
        </div>
    </div>

    <div class="clock-panel">
        <h2>WORLD CLOCK</h2>
        
        <div class="clock-item">
            <div class="cleanslate w24tz-current-time w24tz-middle" style="display: inline-block !important; visibility: hidden !important; min-width:300px !important; min-height:145px !important;"><p><a href="//24timezones.com/Tokyo/time" style="text-decoration: none" class="clock24" id="tz24-1775196657-c1248-eyJob3VydHlwZSI6IjI0Iiwic2hvd2RhdGUiOiIxIiwic2hvd3NlY29uZHMiOiIwIiwiY29udGFpbmVyX2lkIjoiY2xvY2tfYmxvY2tfY2I2OWNmNTlmMTA4NTU5IiwidHlwZSI6ImRiIiwibGFuZyI6ImVuIn0=" title="Tokyo time" target="_blank" rel="nofollow">Tokyo</a></p><div id="clock_block_cb69cf59f108559"></div></div>
        </div>

        <div class="clock-item">
            <div class="cleanslate w24tz-current-time w24tz-middle" style="display: inline-block !important; visibility: hidden !important; min-width:300px !important; min-height:145px !important;"><p><a href="//24timezones.com/State-of-New-York/time" style="text-decoration: none" class="clock24" id="tz24-1775196633-su27-eyJob3VydHlwZSI6IjI0Iiwic2hvd2RhdGUiOiIxIiwic2hvd3NlY29uZHMiOiIwIiwiY29udGFpbmVyX2lkIjoiY2xvY2tfYmxvY2tfY2I2OWNmNTlkOTczMzA5IiwidHlwZSI6ImRiIiwibGFuZyI6ImVuIn0=" title="timezone - New York" target="_blank" rel="nofollow">New York</a></p><div id="clock_block_cb69cf59d973309"></div></div>
        </div>

        <div class="clock-item">
            <div class="cleanslate w24tz-current-time w24tz-middle" style="display: inline-block !important; visibility: hidden !important; min-width:300px !important; min-height:145px !important;"><p><a href="//24timezones.com/Los-Angeles/time" style="text-decoration: none" class="clock24" id="tz24-1775196699-c1137-eyJob3VydHlwZSI6IjI0Iiwic2hvd2RhdGUiOiIxIiwic2hvd3NlY29uZHMiOiIwIiwiY29udGFpbmVyX2lkIjoiY2xvY2tfYmxvY2tfY2I2OWNmNWExYjg0ZWI3IiwidHlwZSI6ImRiIiwibGFuZyI6ImVuIn0=" title="World Time :: Los Angeles" target="_blank" rel="nofollow">Los Angeles</a></p><div id="clock_block_cb69cf5a1b84eb7"></div></div>
        </div>

        <div class="clock-item">
            <div class="cleanslate w24tz-current-time w24tz-middle" style="display: inline-block !important; visibility: hidden !important; min-width:300px !important; min-height:145px !important;"><p><a href="//24timezones.com/London/time" style="text-decoration: none" class="clock24" id="tz24-1775196769-c1136-eyJob3VydHlwZSI6IjI0Iiwic2hvd2RhdGUiOiIxIiwic2hvd3NlY29uZHMiOiIwIiwiY29udGFpbmVyX2lkIjoiY2xvY2tfYmxvY2tfY2I2OWNmNWE2MTVhMjk0IiwidHlwZSI6ImRiIiwibGFuZyI6ImVuIn0=" title="London what time is now" target="_blank" rel="nofollow">London</a></p><div id="clock_block_cb69cf5a615a294"></div></div>
        </div>

        <div class="clock-item">
            <div class="cleanslate w24tz-current-time w24tz-middle" style="display: inline-block !important; visibility: hidden !important; min-width:300px !important; min-height:145px !important;"><p><a href="//24timezones.com/Sydney/time" style="text-decoration: none" class="clock24" id="tz24-1775196790-c1240-eyJob3VydHlwZSI6IjI0Iiwic2hvd2RhdGUiOiIxIiwic2hvd3NlY29uZHMiOiIwIiwiY29udGFpbmVyX2lkIjoiY2xvY2tfYmxvY2tfY2I2OWNmNWE3NjVjYjE4IiwidHlwZSI6ImRiIiwibGFuZyI6ImVuIn0=" title="Sydney current time" target="_blank" rel="nofollow">Sydney</a></p><div id="clock_block_cb69cf5a765cb18"></div></div>
        </div>

        <div class="clock-item">
            <div class="cleanslate w24tz-current-time w24tz-middle" style="display: inline-block !important; visibility: hidden !important; min-width:300px !important; min-height:145px !important;"><p><a href="//24timezones.com/Beijing/time" style="text-decoration: none" class="clock24" id="tz24-1775196855-c133-eyJob3VydHlwZSI6IjI0Iiwic2hvd2RhdGUiOiIxIiwic2hvd3NlY29uZHMiOiIwIiwiY29udGFpbmVyX2lkIjoiY2xvY2tfYmxvY2tfY2I2OWNmNWFiNzViMGIzIiwidHlwZSI6ImRiIiwibGFuZyI6ImVuIn0=" title="Beijing time zone" target="_blank" rel="nofollow">Beijing</a></p><div id="clock_block_cb69cf5ab75b0b3"></div></div>
        </div>

    </div>
</div>

<script type="text/javascript" src="//w.24timezones.com/l.js" async></script>

</body>
</html>
