# Packet Tracer Project : Investigate the TCP/IP and OSI Models in Action
## Project Overview
This network simulation in Packet Tracer activity comprehensively explores network protocols in great detail. It analyses HTTP web traffic by observing how data is encapsulated and transmitted throughout the OSI Model layers. It explores port numbers, IP addresses, and MAC addresses, DNS, ARP, and TCP protocols in web communication process.
rations from routers and switches for easy review.
## Objectives

* Examine HTTP Web Traffic 
* Display Elements of the TCP/IP Protocol Suite 

## Background

This Packet Tracer simulation activity provides a foundational understanding of the TCP/IP protocol suite and its relationship to the OSI model.

In **Simulation mode**, Packet Tracer allows users to:
* View data contents as they are sent across the network at each layer.
* "Stop time" to step through networking events.
* Visualize data as it's broken down into smaller pieces (Protocol Data Units - PDUs) and reassembled at the destination.
* Observe the encapsulation process.

This activity guides the user through requesting a web page from a web server using a client PC's web browser application.

## Instructions

### Part 1: Examine HTTP Web Traffic

In this part, you will use Packet Tracer (PT) Simulation mode to generate web traffic and examine HTTP. 

#### Step 1: Switch from Realtime to Simulation mode.

1.  Click the **Simulation mode** icon in the lower right corner of the Packet Tracer interface to switch from Realtime mode[cite: 9, 13]. [cite_start](PT always starts in Realtime mode, where protocols operate with realistic timings ).
2.  Select **HTTP** from the **Event List Filters**.
    * If HTTP is not the only visible event, click the **Edit Filters** button at the bottom of the simulation panel.
    * Click the **Show All/None** check box until all boxes are cleared, then select **HTTP** from the **Misc** tab of the Edit Filters window.
    * Close the Edit Filters window by clicking the **X** in the upper right corner. The Visible Events should now only display HTTP.

#### Step 2: Generate web (HTTP) traffic.

[cite_start]The Simulation Panel's Event List will populate with events as traffic is generated.

1.  Click **Web Client** in the far left pane.
2.  Click the **Desktop** tab and then click the **Web Browser** icon to open it.
3.  In the URL field, enter `www.osi.local` and click **Go**.
4.  Click the **Capture/Forward** button four times. This button is located on the right side of the blue band below the topology window. There should now be four events in the Event List.

#### Step 3: Explore the contents of the HTTP packet.

1.  Click the first colored square box under the **Event List > Type** column. (You may need to expand the Simulation Panel or use the scrollbar ).
2.  The "PDU Information at Device: Web Client" window will appear. At the start of a transmission, this window will have two tabs: **OSI Model** and **Outbound PDU Details**.
3.  Ensure the **OSI Model** tab is selected.
4.  Under the **Out Layers** column, click **Layer 7**.

    * **Question:** What information is listed in the numbered steps directly below the In Layers and Out Layers boxes for Layer 7? 
    * **Question:** What is the Dst Port value for Layer 4 under the Out Layers column? 
    * **Question:** What is the Dest. IP value for Layer 3 under the Out Layers column? 
    * **Question:** What information is displayed at Layer 2 under the Out Layers column? 
5.  Click the **Outbound PDU Details** tab. Information here reflects the TCP/IP model layers.
    * **Note:** The Ethernet II section in Outbound PDU Details provides more detailed information than Layer 2 on the OSI Model tab. DEST MAC and SRC MAC values are found here.
    * **Question:** What is the common information listed under the IP section of PDU Details as compared to the information listed under the OSI Model tab?  With which layer is it associated? 
    * **Question:** What is the common information listed under the TCP section of PDU Details, as compared to the information listed under the OSI Model tab, and with which layer is it associated? 
    * **Question:** What is the Host listed under the HTTP section of the PDU Details?  What layer would this information be associated with under the OSI Model tab? 

6.  Click the next colored square box under the **Event List > Type** column. Only Layer 1 should be active, indicating the device is moving the frame onto the network.
7.  Advance to the next HTTP Type box in the Event List and click its colored square box.
    * This window will contain both **In Layers** and **Out Layers**.
    * Observe the upward-pointing arrow under the In Layers column, indicating the data's travel direction. Scroll through the layers, noting previously viewed items.
    * The arrow at the top of the column pointing to the right signifies the server sending information back to the client.
    * **Question:** Comparing the information displayed in the In Layers column with that of the Out Layers column, what are the major differences? 
8.  Click the **Inbound and Outbound PDU Details** tab and review the PDU details.
9.  Click the last colored square box under the **Info** column.
    * **Question:** How many tabs are displayed with this event? Explain. 
### Part 2: Display Elements of the TCP/IP Protocol Suite
In this part, you will use Packet Tracer Simulation mode to view and examine other protocols within the TCP/IP suite. 
#### Step 1: View Additional Events
1.  Close any open PDU information windows.
2.  In the **Event List Filters > Visible Events** section, click **Show All/None**.
    * **Question:** What additional Event Types are displayed? 
        * **Note:** These entries include protocols like Address Resolution Protocol (ARP) for MAC address requests, DNS for name-to-IP address conversion (e.g., `www.osi.local` to its IP), and additional TCP events for managing communication sessions (connecting, agreeing on parameters, disconnecting). Packet Tracer has over 35 possible event types available.

3.  Click the first **DNS** event in the Type column. Explore the **OSI Model** and **PDU Detail** tabs, noting the encapsulation process.
    * With Layer 7 highlighted on the OSI Model tab, observe the description below the In Layers and Out Layers (e.g., "1. The DNS client sends a DNS query to the DNS server."). This description helps understand the communication process.

4.  Click the **Outbound PDU Details** tab.
    * **Question:** What information is listed in the NAME field in the DNS QUERY section? 

5.  Click the last **DNS Info** colored square box in the event list.
    * **Question:** At which device was the PDU captured? 
    * **Question:** What is the value listed next to ADDRESS: in the DNS ANSWER section of the Inbound PDU Details? 
6.  Find the first **HTTP** event in the list and click the colored square box of the **TCP** event immediately following it.
7.  Highlight **Layer 4** in the OSI Model tab.
    * **Question:** In the numbered list directly below the In Layers and Out Layers, what information is displayed under items 4 and 5? 
    * **Note:** TCP manages the connection and disconnection of the communication channel, among other responsibilities. This event shows the communication channel has been ESTABLISHED.

8.  Click the last **TCP** event. Highlight **Layer 4** in the OSI Model tab. Examine the steps listed directly below In Layers and Out Layers.
    * **Question:** What is the purpose of this event, based on the information provided in the last item in the list (should be item 4)? 

## Challenge Questions

This simulation demonstrated a web session between a client and a server on a Local Area Network (LAN). Clients request specific services running on the server, and the server must be configured to listen on particular ports for these requests.

* Based on the information inspected during the Packet Tracer capture, what port number is the Web Server listening on for the web request? (Hint: Look at Layer 4 in the OSI Model tab for port information ).
* What port is the Web Server listening on for a DNS request?
