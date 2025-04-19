# Packet Filtering in Wireshark 

## Introduction 
Wireshark offers a robust filtering engine that helps users concentrate on specific traffic events. It has two types of filters: capture filters, which capture packets based on the filter criteria, and display filters, which display packets based on the filter criteria. This summary focuses on the basic usage of display filters to assist analysts. 

## Key Points 

## Types of Filters 
• Capture Filters: Capture only packets that meet the specified criteria. 

• Display Filters: View only packets that meet the specified criteria while already captured. 

## Basic Filtering Methods 
1. Filters as Queries: Users can create specific queries for protocols using Wireshark’s official references. 
2. Right-Click Menu Usage: A user-friendly option for filtering without writing queries. The rule to remember is: “If you can click on it, you can filter and copy it. ” 

## Apply as Filter 

• Allows users to filter traffic by clicking on a field in a captured packet.

• Accessed through the right-click menu or `Analyse -&gt; Apply as Filter`.

• Automatically generates a query to show selected packets and hide others. 

## Conversation Filter 

• Filters based on a single packet entity using the 'Apply as Filter' option. 

• To investigate linked packets related by IP addresses and port numbers, use the Conversation Filter, accessible through the right-click menu or `Analyse -&gt; Conversation Filter`. 

## Colourise Conversation 

• Similar to the Conversation Filter, but this option highlights related packets without reducing the view. 

• Change packet colors based on linkages with the `right-click menu` or by selecting `View -&gt; Colourise Conversation`. 

• Reset color changes using `View -&gt; Colourise Conversation -&gt; Reset Colourisation`. 

## Prepare as Filter 

• Similar to 'Apply as Filter' but does not execute the filter right away. 

• Adds the query to the filter pane and awaits execution by pressing enter or choosing another filtering option. 

## Apply as Column 

• Allows users to add additional information columns to the packet list pane. 

• Uses the right-click menu or `Analyse -&gt; Apply as Column` to display specific values across packets. 

## Follow Stream 

• Enables the reconstruction of streams to view traffic as it was presented at the application level. 

• Use the right-click menu or `Analyse -&gt; Follow TCP/UDP/HTTP Stream` to follow protocol streams. 

• Showcases traffic in a separate window, highlighting server-originating packets in blue and client-originating packets in red. 

• Automatically applies the necessary filter for viewing the stream; use the 'X button' to remove the filter and see all packets again. 

## Conclusion 
Wireshark's filtering capabilities, including various methods to apply filters, create columns, and follow streams, allow analysts to effectively analyze network traffic and focus on specific events of interest. Understanding these tools enhances the efficiency of packet analysis.