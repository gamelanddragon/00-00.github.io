<!DOCTYPE html>
<html lang="hu">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cisco Packet Tracer Portfólió - 1.csoport_r_d_v</title>
    <style>
        :root {
            --cisco-blue: #049fd9;
            --cisco-dark: #005073;
            --light-gray: #f4f4f4;
            --dark-gray: #333;
            --accent-orange: #ffa94d;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #e6f7ff 0%, #f0f8ff 100%);
            color: #333;
            line-height: 1.6;
            padding: 20px;
            min-height: 100vh;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: white;
            border-radius: 12px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            overflow: hidden;
        }
        
        header {
            background: linear-gradient(135deg, var(--cisco-dark), var(--cisco-blue));
            color: white;
            padding: 2.5rem 0;
            text-align: center;
            position: relative;
        }
        
        header h1 {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }
        
        header p {
            font-size: 1.2rem;
            opacity: 0.9;
        }
        
        .cisco-logo {
            position: absolute;
            top: 20px;
            right: 30px;
            font-size: 2rem;
            font-weight: bold;
        }
        
        .content {
            padding: 30px;
        }
        
        h2 {
            color: var(--cisco-dark);
            border-bottom: 3px solid var(--cisco-blue);
            padding-bottom: 10px;
            margin: 30px 0 20px 0;
            display: inline-block;
        }
        
        h3 {
            color: var(--cisco-blue);
            margin: 20px 0 15px 0;
        }
        
        .section {
            margin-bottom: 40px;
        }
        
        .device-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin: 20px 0;
        }
        
        .device-card {
            background: var(--light-gray);
            border-radius: 8px;
            padding: 20px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .device-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 15px rgba(0, 0, 0, 0.1);
        }
        
        .device-card h4 {
            color: var(--cisco-dark);
            margin-bottom: 10px;
            border-bottom: 2px solid var(--cisco-blue);
            padding-bottom: 8px;
        }
        
        .config-table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.05);
            border-radius: 8px;
            overflow: hidden;
        }
        
        .config-table th, .config-table td {
            border: 1px solid #ddd;
            padding: 12px 15px;
            text-align: left;
        }
        
        .config-table th {
            background-color: var(--cisco-blue);
            color: white;
            font-weight: 600;
        }
        
        .config-table tr:nth-child(even) {
            background-color: #f8fbff;
        }
        
        .config-table tr:hover {
            background-color: #e6f2ff;
        }
        
        .cli-code {
            background: #2d2d2d;
            color: #f8f8f2;
            padding: 20px;
            border-radius: 8px;
            font-family: 'Consolas', 'Monaco', monospace;
            overflow-x: auto;
            margin: 20px 0;
            line-height: 1.5;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        
        .cli-code .comment {
            color: #75715e;
            font-style: italic;
        }
        
        .cli-code .command {
            color: #a6e22e;
        }
        
        .fun-fact {
            background: linear-gradient(135deg, #fff4e6 0%, #ffe8cc 100%);
            padding: 25px;
            border-radius: 8px;
            border-left: 5px solid var(--accent-orange);
            margin: 30px 0;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.05);
        }
        
        .comparison-table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.05);
        }
        
        .comparison-table th, .comparison-table td {
            border: 1px solid #ddd;
            padding: 12px 15px;
            text-align: center;
        }
        
        .comparison-table th {
            background-color: var(--cisco-dark);
            color: white;
        }
        
        .comparison-table tr:nth-child(even) {
            background-color: #f8fbff;
        }
        
        footer {
            text-align: center;
            margin-top: 40px;
            padding: 20px;
            background: var(--cisco-dark);
            color: white;
            border-radius: 0 0 8px 8px;
        }
        
        .protocol-badge {
            display: inline-block;
            background: var(--cisco-blue);
            color: white;
            padding: 5px 10px;
            border-radius: 20px;
            font-size: 0.9rem;
            margin: 5px;
        }
        
        @media (max-width: 768px) {
            .device-grid {
                grid-template-columns: 1fr;
            }
            
            header h1 {
                font-size: 2rem;
            }
            
            .config-table, .comparison-table {
                font-size: 0.9rem;
            }
            
            .cisco-logo {
                position: relative;
                top: 0;
                right: 0;
                margin-top: 15px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>Cisco Packet Tracer Portfólió</h1>
            <p>1.csoport_r_d_v - Hálózati konfiguráció és beállítások</p>
            <div class="cisco-logo">Cisco</div>
        </header>
        
        <div class="content">
            <div class="section">
                <h2>Alapleírások</h2>
                <p>A hálózati infrastruktúra a következő eszközöket tartalmazza:</p>
                
                <div class="device-grid">
                    <div class="device-card">
                        <h4>WRT300N Router</h4>
                        <ul>
                            <li>1 db Internet Port</li>
                            <li>3 db Ethernet Port</li>
                            <li>Wireless kapcsolat</li>
                        </ul>
                    </div>
                    
                    <div class="device-card">
                        <h4>Switch (2960-24-TT)</h4>
                        <ul>
                            <li>24 db FastEthernet Port</li>
                            <li>3 db GigabitEthernet Port</li>
                        </ul>
                    </div>
                    
                    <div class="device-card">
                        <h4>Számítógépek</h4>
                        <ul>
                            <li>2 db PC</li>
                            <li>1 db FastEthernet Port</li>
                        </ul>
                    </div>
                    
                    <div class="device-card">
                        <h4>Mobil eszköz</h4>
                        <ul>
                            <li>1 db SmartPhone</li>
                            <li>Wireless kapcsolat</li>
                        </ul>
                    </div>
                </div>
            </div>
            
            <div class="section">
                <h2>Beállítások</h2>
                
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
                
                <h3>Használt protokollok</h3>
                <div>
                    <span class="protocol-badge">DHCP - OSI 3. réteg</span>
                    <span class="protocol-badge">IP - OSI 3. réteg</span>
                </div>
            </div>
            
            <div class="section">
                <h2>Fun Fact ☺</h2>
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
                <h2>Portvédelem - Switch (CLI)</h2>
                <div class="cli-code">
                    <span class="comment">! Első mindig a bekapcsolás:</span><br>
                    <span class="command">enable</span><br>
                    <span class="command">conf t</span><br><br>
                    
                    <span class="comment">! Port kiválasztása:</span><br>
                    <span class="command">interface FastEthernet0/1</span><br><br>
                    
                    <span class="comment">! Engedélyezd a portvédelmet:</span><br>
                    <span class="command">switchport port-security</span><br><br>
                    
                    <span class="comment">! Max MAC cím:</span><br>
                    <span class="command">switchport port-security maximum 1</span><br><br>
                    
                    <span class="comment">! Dinamikus MAC cím tanulása:</span><br>
                    <span class="command">switchport port-security mac-address sticky</span><br><br>
                    
                    <span class="comment">! (OSI-modell szerint: 2. réteg)</span>
                </div>
            </div>
        </div>
        
        <footer>
            <p>Generálva: 2025.09.12 | 1.csoport_r_d_v | Cisco Packet Tracer Portfólió</p>
        </footer>
    </div>
</body>
</html>
