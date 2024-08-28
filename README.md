# Ring-topologi

![image](https://github.com/user-attachments/assets/64cbd9e3-ed23-429d-a2ee-135d82b9f7ea)


  h1>Network Diagram Explanation: 4-Section Ring Topology</h1>

  <p>The diagram illustrates the initial setup for a 4-section ring topology network. This topology is designed for enhanced redundancy and reliability, ensuring continuous network operation even if one link in the ring fails.</p>

   <h2>Key Components:</h2>

   <h3>1. WAN Connections:</h3>
    <ul>
        <li>Two possible WAN IP addresses (<code>185.221.103.70</code> and <code>185.221.103.72</code>) are connected to the internet via two Fortinet firewall devices.</li>
        <li>The Fortinet devices connect to the internal network through routers R1 and R2.</li>
    </ul>

  <h3>2. Routers (R1 and R2):</h3>
    <ul>
        <li><strong>Router R1:</strong> Connected to the WAN via IP <code>185.221.103.72</code>, and internally uses IP <code>192.168.1.2</code>.</li>
        <li><strong>Router R2:</strong> Connected to the WAN via IP <code>185.221.103.70</code>, and internally uses IP <code>192.168.1.3</code>.</li>
        <li>These routers are linked via a direct connection (shown as <code>192.168.1.1</code>) to ensure internal network redundancy.</li>
    </ul>

   <h3>3. Core Switches:</h3>
    <ul>
        <li><strong>Switch:</strong> Acts as a central switch, connected to routers R1 (<code>Gi0/0</code>) and R2 (<code>Gi0/1</code>). This switch connects to various network segments to distribute traffic across the network.</li>
        <li><strong>Node7:</strong> This switch is connected to the central switch (<code>Gi1/2</code>) and extends the network further into the ring topology.</li>
    </ul>

   <h3>4. Distribution Switches (S-D1, S-D2, S-D3):</h3>
    <ul>
        <li>These switches (<code>S-D1</code>, <code>S-D2</code>, <code>S-D3</code>) are connected to the core switches, providing connections to various segments in the network. Each distribution switch has several devices connected (not all shown).</li>
    </ul>

   <h3>5. Access Switches (SW-LAN10, SW-LAN13, SW-LAN14):</h3>
    <ul>
        <li>These switches (<code>SW-LAN10</code>, <code>SW-LAN13</code>, <code>SW-LAN14</code>) are connected in a loop to the distribution switches. They form part of the ring, ensuring that even if one connection is broken, the network can reroute traffic through another path.</li>
    </ul>

  <h3>6. Linux Server:</h3>
    <ul>
        <li>A Linux server is connected to the network via <code>Node7</code>. This server is likely used for network management, monitoring, or other critical services.</li>
    </ul>

  <h2>Topology Overview:</h2>
    <ul>
        <li><strong>Ring Topology:</strong> The network is set up to form a ring between the switches (<code>SW-LAN10</code>, <code>SW-LAN13</code>, and <code>SW-LAN14</code>), which provides redundancy. If one link fails, traffic can be rerouted in the opposite direction to maintain network connectivity.</li>
        <li><strong>Redundancy:</strong> The use of multiple switches and connections in a ring topology ensures that the network is robust and can handle failures without significant downtime.</li>
        <li><strong>Scalability:</strong> The topology allows for easy addition of more switches and devices without disrupting the network's overall operation.</li>
    </ul>

</body>
</html>



