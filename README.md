# WE 755A PBX Switching Power Supply


# Overview

The Western Electric 755A PBX typically received -24VDC and ringing current from the local central office via the outside plant.

This project is similar to the [OKI AC125A Power Supply](https://github.com/hharte/ac125a_ps) designed several years ago.  The OKI requires a single -48VDC supply, whereas the 755A requires -24VDC and ringing current.

Use a Mean Well RSP-200-24 switching supply capable of supplying 24VDC at 8.4A.  Create a 26” x 2” mounting plate to mount the power supply and meters for measuring current and voltage.

![alt_text](https://raw.githubusercontent.com/hharte/we755a_ps/main/photos/we755a_ps.jpg "image_tooltip")


# Mounting Plate

The mounting plate was designed with Front Panel Designer and ordered from [https://www.frontpanelexpress.com](https://www.frontpanelexpress.com/) and received within a few days.


# Components



* [Mean Well RSP-200-24](https://www.digikey.com/en/products/detail/mean-well-usa-inc/rsp-200-24/7706308) Power Supply
* [Illuminated Power Switch](https://www.digikey.com/en/products/detail/e-switch/RBW2ABLKGILFF1/2639098)
* [Two LED DC panel meters](https://www.amazon.com/dp/B01DDQM6Z4)
* [24V PBX Ring Generator](https://github.com/hharte/pbx_ring_gen)
* 3D-printed [power supply guard](https://github.com/hharte/we755a_ps/blob/main/ps_guard.stl).
* 3-prong (grounded) line cord.  Scrounge or [purchase](https://www.amazon.com/Pinfox-Universal-Appliance-Replacement-Pigtail/dp/B06XRKXLVV).
* [M4 tapered head screws and nuts](https://www.amazon.com/gp/product/B07S18NHP5).
* [M3 tapered head screws](https://www.amazon.com/Kindroufly-Pieces-Countersunk-Washers-Assortment/dp/B0BLCFZF14).
* [Crimp ring terminals and female spade terminals](https://www.amazon.com/Insulated-Assortment-Disconnect-Solderless-Electrical/dp/B0CP78VXNQ).
* [Heat-shrink tubing](https://www.amazon.com/650pcs-Shrink-Tubing-innhom-Approved/dp/B07WWWPR2X).


# Assembly

Attach the Mean Well RSP-200-24 power supply to the rear of the power supply front panel using two M4 tapered head screws, 5 mm in length.  Since we want a -24VDC output, connect the power supply’s **_+V_** terminal to the earth ground terminal.  Be sure to use a 3-prong (grounded) cord.  PBX GRD (ground) is the three **_+V_** terminals, while -24VDC is the three **_-V_** terminals.


<table>
  <tr>
   <td><strong><em>Terminal</em></strong>
   </td>
   <td><strong><em>Legend</em></strong>
   </td>
   <td><strong><em>Description</em></strong>
   </td>
   <td><strong><em>Use</em></strong>
   </td>
  </tr>
  <tr>
   <td>1
   </td>
   <td>L
   </td>
   <td>AC Line
   </td>
   <td>AC Line (black) Input, to rocker switch.
   </td>
  </tr>
  <tr>
   <td>2
   </td>
   <td>N
   </td>
   <td>AC Neutral
   </td>
   <td>AC Neutral (white) Input, to rocker switch.
   </td>
  </tr>
  <tr>
   <td>3
   </td>
   <td>FG
   </td>
   <td>Earth Ground
   </td>
   <td>Earth Ground (green) to line cord, and tied to +V.
   </td>
  </tr>
  <tr>
   <td rowspan="3" >4
<p>
5
<p>
6
   </td>
   <td rowspan="3" ><strong><em>-V</em></strong>
   </td>
   <td rowspan="3" >DC Output (-)
   </td>
   <td rowspan="3" >Meter black leads.
<p>
-24VDC (Feeds the PBX Ring Generator and the 755A PBX)
   </td>
  </tr>
  <tr>
  </tr>
  <tr>
  </tr>
  <tr>
   <td rowspan="3" >7
<p>
8
<p>
9
   </td>
   <td rowspan="3" ><strong><em>+V</em></strong>
   </td>
   <td rowspan="3" >DC Output (+)
   </td>
   <td rowspan="3" >Tie this terminal to FG.
<p>
Meter red leads.
<p>
GRD (Ground)
   </td>
  </tr>
  <tr>
  </tr>
  <tr>
  </tr>
</table>


Both the Line and Neutral should be switched using the 2-pole lighted rocker switch.  Use crimped ring terminals for all terminal block connections.  Use female spade connectors for the switch connections.  Insulate all connections with heat-shrink tubing for safety.

To install the LED voltage and current meters, remove the meter circuit board from the plastic housing by carefully bending the tabs.  Pop the plastic housing into the mounting holes, and then carefully re-install the circuit board assembly, taking care not to crack the LED diffuser panel.

When connecting the panel meters, be sure that the red wire on the meter is connected to the more positive terminal (**_+V_**) of the power supply and connect the black wire of the meter to the more negative terminal (**_-V_**.)

The current meter has a range of 0-100A.  As the 755A draws nowhere near this amount of current, and in fact, the Mean Well RSP-200-24 is only capable of supplying 8.4A, wrap the -24V lead 10 times around the hall effect sensor.  This improves the accuracy of the current meter with a range of 0-10A.  The only drawback to this is that the decimal point is in the wrong place.

3D-print the [power supply guard](https://github.com/hharte/we755a_ps/blob/main/ps_guard.stl): [For safety](https://en.wikipedia.org/wiki/UL_94), it’s a good idea to print this using [V-0 PETG](https://prusament.com/materials/prusament-petg-v0/).  Attach using a 10 mm M4 tapered head screw and nut.  The fourth M4 hole in the mounting plate can be used to attach a wire fastener using an M4 tapered head screw and nut.

Attach the [PBX Ring Generator](https://github.com/hharte/pbx_ring_gen) using four M3 tapered head screws, 5 mm in length.


# Other WE 755A Projects

[WE 755A DTMF Converter](https://github.com/hharte/we755a_dtmf)
