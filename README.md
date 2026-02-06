<p align="center">
<img width="901" height="274" alt="Screenshot 2026-02-06 164314" src="https://github.com/user-attachments/assets/cec2ced5-3323-4d84-a2a2-b60b96955907" />
</p>
<h1><u>Milestone 3: HQ Access Switching</u></h1>
    <p>Second phase, we will install 3 Cisco WS-C2960-24TT layer 2 access switches.</p>
    <h2><strong><u>Configuration Steps</u></strong></h2>
    <p>Step 1: Rack, Mount, and Power On All 3 Switches</p>
    <p>Step 2: Basic Switch Configurations (Hostname, NTP, Domain-Name, SSH, Etc)</p>
    <p>Step 3: Configure VLAN Trunking Protocol (VTP) Client</p>
    <p>Step 4: Create MGMT VLAN Interface</p>
    <p>Step 5: Configure Default Gateway</p>
    <p>Step 6: Configure and Connect Trunk Ports</p>
    <p>Step 7: Configure Access Ports</p>
    <h2><strong><u>Implementation</u></strong></h2>
        <h3>Step 1: Rack, Mount, and Power On All 3 Switches</h3>
            <p>- First, we'll add three 2960 switches to the topology by dragging and dropping them into the Headquarters section of the lab. Place them side by side and label them as HQ-ASW1, HQ-ASW2, and HQ-ASW3.</p>
                <img width="849" height="976" alt="Screenshot 2026-02-06 170658" src="https://github.com/user-attachments/assets/7704547b-449d-4bf6-a9e5-b3cb783f1ac2" />
        <h3>Step 2: Basic Switch Configurations (Hostname, NTP, Domain-Name, SSH, Etc)</h3>
            <p>- In this step, we did basic configuration for both of the switches including changing their hostnames, setting their time zones, enabling SSH, setting domain names, adding securiting to console and vty lines for SSH, and creating user profiles with a password the devices</p>
                <img width="867" height="896" alt="Screenshot 2026-02-06 171129" src="https://github.com/user-attachments/assets/3ae0553b-ebfd-4adc-8154-4c4cac1bd1b1" />
                <img width="870" height="905" alt="Screenshot 2026-02-06 171255" src="https://github.com/user-attachments/assets/bfbb60cc-eb80-42e5-96e2-53c630386aa8" />
                <img width="872" height="907" alt="Screenshot 2026-02-06 171401" src="https://github.com/user-attachments/assets/f6f42ebc-d37f-4d1f-becb-f746c8e8955f" />
        <h3>Step 3: Configure VLAN Trunking Protocol (VTP) Client</h3>
            <p>- Next we will configure VTP on these switches to receive and sync all VLAN updates from the vtp server we configured in the first milestone.</p>
                <img width="873" height="618" alt="Screenshot 2026-02-06 172047" src="https://github.com/user-attachments/assets/286483a4-c123-4d64-91e9-1392d67fe7a6" />
                <img width="871" height="616" alt="Screenshot 2026-02-06 172212" src="https://github.com/user-attachments/assets/0239a279-7874-41fe-9cde-7602be6e307d" />
                <img width="871" height="890" alt="Screenshot 2026-02-06 172337" src="https://github.com/user-attachments/assets/92834966-d56d-4f3a-b417-4e1c1a37db5f" />
        <h3>Step 4: Create MGMT VLAN Interface</h3>
            <p>- For this step, we will now create these VLANs on both switches to segment a single physical network infrastructure into multiple, isolated, logical networks, improving performance, security, and management.</p>
                <img width="869" height="920" alt="Screenshot 2026-02-05 180818" src="https://github.com/user-attachments/assets/9bf9ce07-cc81-4e64-ad62-6f9865424ea9" />
                <img width="870" height="884" alt="Screenshot 2026-02-05 181021" src="https://github.com/user-attachments/assets/c47cb564-3475-49e1-8b9e-a03253684591" />
        <h3>Step 5: Configure Default Gateway</h3>
            <p>- In this step, we will configure the VLAN Trunking Protocol Server to centralize and automate the management of VLAN configurations (add, delete, rename) across all switches in this topology.</p>
                <img width="869" height="956" alt="Screenshot 2026-02-05 181801" src="https://github.com/user-attachments/assets/fafc602d-5167-46e5-978a-5a821b52ddab" />
                <img width="868" height="954" alt="Screenshot 2026-02-05 182024" src="https://github.com/user-attachments/assets/5d99222e-830f-4727-a75b-4fa69ab05f5b" />
        <h3>Step 6: Configure and Connect Trunk Ports</h3>
            <p>- For this step, we will create the VLAN interfaces for the corresponding VLANs we have created, so that we can in fact route traffic between the different VLANs, enabling inter-VLAN communication.</p>
                <img width="866" height="744" alt="Screenshot 2026-02-05 183818" src="https://github.com/user-attachments/assets/163ad1d5-f493-45e2-8456-a2ea8ab5bd31" />
                <img width="867" height="729" alt="Screenshot 2026-02-05 183940" src="https://github.com/user-attachments/assets/644f4b1e-93ef-44ef-8cc7-b691a4c8ffe8" />
        <h3>Step 7: Configure Access Ports</h3>
            <p>- For this next step, we will configure HSRP under all VLAN interfaces to share an IP address between the switches to provide first-hop gateway redundancy, ensuring uninterrupted network connectivity if a primary switch were to fail. This will create a virtual IP and MAC address shared between the switches, allowing hosts to maintain a consistent default gateway IP, thereby minimizing downtime during network failures.</p>
                <img width="866" height="761" alt="Screenshot 2026-02-05 185513" src="https://github.com/user-attachments/assets/7286b27b-ce25-455d-996d-57ad053ce965" />
                <img width="867" height="797" alt="Screenshot 2026-02-05 185911" src="https://github.com/user-attachments/assets/c42797f9-9c5d-4a12-ae2c-0885ffd90a3d" />
            <p><em>- For the priority 255 command, it will force the switch to be the primary gateway, while configuring priority 0 will ensure it is the last resort for the specific vlan. The preempt command allows the higher priority switch to immediately seize control from the active switch with lower the priority if there happened to be a device failure.</em></p>
        










            












 





