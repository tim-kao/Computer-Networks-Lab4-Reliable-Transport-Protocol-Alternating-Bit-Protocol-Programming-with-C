# Computer-Networks-Lab4-Reliable-Transport-Protocol-Alternating-Bit-Protocol-Programming-with-C

## Overview ##
Lab 4: Alternating-Bit-Protocol. \
An SMTP client delivers email with text and image content.
Implement the ABP state machine ![image](https://github.com/tim-kao/Computer-Networks-Lab4-Reliable-Transport-Protocol-Alternating-Bit-Protocol-Programming-with-C/blob/main/figpa21.gif)
## Demo ##
Sample output(10 messages have been ACK'ed correctly at the receiver, a loss probability of
0.1, and a corruption probability of 0.3, and a trace level of 2.)
[Output log](https://github.com/tim-kao/Computer-Networks-Lab4-Reliable-Transport-Protocol-Alternating-Bit-Protocol-Programming-with-C/blob/main/output.log)

##  Usage Examples ##

   
## Methods ##
Based on the [skeleton code](https://github.com/tim-kao/Computer-Networks-Lab4-Reliable-Transport-Protocol-Alternating-Bit-Protocol-Programming-with-C/blob/main/prog2.c), the methods are implemented in the following.
1. A_output(message), where message is a structure of type msg, containing data to be sent to the B-side. This routine will be called whenever the upper layer at the sending side (A) has a message to send. It is the job of your protocol to insure that the data in such a message is delivered in-order, and correctly, to the receiving side upper layer.
A_input(packet), where packet is a structure of type pkt. This routine will be called whenever a packet sent from the B-side (i.e., as a result of a tolayer3() being done by a B-side procedure) arrives at the A-side. packet is the (possibly corrupted) packet sent from the B-side.
2. A_timerinterrupt()  This routine will be called when A's timer expires (thus generating a timer interrupt). You'll probably want to use this routine to control the retransmission of packets. See starttimer() and stoptimer() below for how the timer is started and stopped.
3. A_init() This routine will be called once, before any of your other A-side routines are called. It can be used to do any required initialization.
4. B_input(packet),where packet is a structure of type pkt. This routine will be called whenever a packet sent from the A-side (i.e., as a result of a tolayer3() being done by a A-side procedure) arrives at the B-side. packet is the (possibly corrupted) packet sent from the A-side.
5. B_init() This routine will be called once, before any of your other B-side routines are called. It can be used to do any required initialization.
   
## Contributor ##
#### [Tim Kao](https://github.com/tim-kao?fbclid=IwAR0lWAvmWe03EtuderoHdKEpYYG8pnl2ca1bN1b5DBfEMP-wFv4kQupl-Jg) (UNI: sk4920)
