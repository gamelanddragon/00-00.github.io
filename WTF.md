<!DOCTYPE html>
<html lang="hu">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cisco Packet Tracer Portfólió - 1.csoport_r_d_v</title>
    <style>
        body {
            font-family: 'Segoe UI', Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 20px;
            color: #333;
            background-color: #f9f9f9;
        }
        .container {
            max-width: 1000px;
            margin: 0 auto;
            background: white;
            padding: 30px;
            box-shadow: 0 0 15px rgba(0,0,0,0.1);
            border-radius: 8px;
        }
        h1 {
            color: #005073;
            text-align: center;
            border-bottom: 3px solid #049fd9;
            padding-bottom: 15px;
            margin-bottom: 30px;
        }
        h2 {
            color: #049fd9;
            border-bottom: 2px solid #eaeaea;
            padding-bottom: 8px;
            margin-top: 25px;
        }
        h3 {
            color: #005073;
        }
        .underline {
            text-decoration: underline;
        }
        .section {
            margin-bottom: 30px;
        }
        .device-list {
            background: #f0f8ff;
            padding: 15px;
            border-radius: 5px;
            border-left: 5px solid #049fd9;
        }
        .config-table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
        }
        .config-table th, .config-table td {
            border: 1px solid #ddd;
            padding: 10px;
            text-align: left;
        }
        .config-table th {
            background-color: #e6f7ff;
        }
        .cli-code {
            background: #2d2d2d;
            color: #f8f8f2;
            padding: 15px;
            border-radius: 5px;
            font-family: 'Consolas', monospace;
            overflow-x: auto;
            margin: 20px 0;
        }
        .fun-fact {
            background: #fff4e6;
            padding: 15px;
            border-radius: 5px;
            border-left: 5px solid #ffa94d;
            margin: 20px 0;
        }
        .comparison-table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
        }
        .comparison-table th, .comparison-table td {
            border: 1px solid #ddd;
            padding: 10px;
            text-align: center;
        }
        .comparison-table th {
            background-color: #e6f7ff;
        }
        footer {
            text-align: center;
            margin-top: 40px;
            color: #666;
            font-size: 0.9em;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Cisco Packet Tracer Portfólió<br>1.csoport_r_d_v</h1>
        
        <div class="section">
            <h2><span class="underline">Alapleírások</span></h2>
            <div class="device-list">
                <h3>Hálózati eszközök:</h3>
                <ul>
                    <li>1 db WRT300N router (1 db Internet Port, 3 db Ethernet Port)</li>
                    <li>1 db Switch (2960-24-TT) (24 db FastEthernet Port, 3 db GigabitEthernet port)</li>
                    <li>2 db PC (1 db FastEthernet Port)</li>
                    <li>1 db SmartPhone (Wireless kapcsolattal)</li>
                </ul>
            </div>
        </div>

        <div class="section">
            <h2><span class="underline">Beállítások</span></h2>
            <table class="config-table">
                <tr>
                    <th>Eszköz</th>
                    <th>IP Cím</th>
                    <th>Maszk</th>
                    <th>Megjegyzés</th>
                </tr>
                <tr>
                    <td>PC0</td>
                    <td>192.168.10.99</td>
                    <td>255.255.255.0</td>
                    <td>Statikus cím</td>
                </tr>
                <tr>
                    <td>PC1</td>
                    <td>DHCP</td>
                    <td>Automatikus</td>
                    <td>DHCP kliens</td>
                </tr>
                <tr>
                    <td>Wireless Router</td>
                    <td>DHCP kiosztás<br>Statikus: 192.168.10.100</td>
                    <td>DHCP<br>Statikus: 255.255.255.0</td>
                    <td>DHCP szerver és statikus cím</td>
                </tr>
                <tr>
                    <td>Phone</td>
                    <td>DHCP (192.168.10.100-149)</td>
                    <td>Automatikus</td>
                    <td>DHCP kliens</td>
                </tr>
            </table>
            
            <p><strong>Protokollok:</strong></p>
            <ul>
                <li>DHCP - OSI 3. réteg</li>
                <li>IP - OSI 3. réteg</li>
            </ul>
        </div>

        <div class="section">
            <h2><span class="underline">Fun Fact ☺</span></h2>
            <div class="fun-fact">
                <h3>IPv4 vs IPv6 összehasonlítás</h3>
                <table class="comparison-table">
                    <tr>
                        <th>Tulajdonság</th>
                        <th>IPv4</th>
                        <th>IPv6</th>
                    </tr>
                    <tr>
                        <td><strong>Címhossz</strong></td>
                        <td>32 bites</td>
                        <td>128 bites</td>
                    </tr>
                    <tr>
                        <td><strong>Címtartomány</strong></td>
                        <td>Korlátozott (~4.3 milliárd cím)</td>
                        <td>Gyakorlatilag kimeríthetetlen</td>
                    </tr>
                    <tr>
                        <td><strong>Alkalmazás</strong></td>
                        <td>Hagyományos hálózatok</td>
                        <td>IoT és minden növekvő internetes eszköz</td>
                    </tr>
                </table>
            </div>
        </div>

        <div class="section">
            <h2><span class="underline">Portvédelem - Switch (CLI)</span></h2>
            <div class="cli-code">
                <p>! Első mindig a bekapcsolás:</p>
                enable<br>
                conf t<br><br>
                
                <p>! Port kiválasztása:</p>
                interface FastEthernet0/1<br><br>
                
                <p>! Engedélyezd a portvédelmet:</p>
                switchport port-security<br><br>
                
                <p>! Max MAC cím:</p>
                switchport port-security maximum 1<br><br>
                
                <p>! Dinamikus MAC cím tanulása:</p>
                switchport port-security mac-address sticky<br><br>
                
                <p>! (OSI-modell szerint: 2. réteg)</p>
            </div>
        </div>

        <footer>
            <p>Generálva: 2025.09.12 | 1.csoport_r_d_v | Cisco Packet Tracer Portfólió</p>
        </footer>
    </div>
</body>
</html>
