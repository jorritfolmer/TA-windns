# TA-windns for Splunk

This CIM compliant TA can be used with Splunk (Enterprise Security) and provides
field extractions, aliases, eventtypes and tags for Windows DNS logging.

It extracts fields and maps to the Network Resolution CIM datamodel.

## Installation

Install this TA on your Splunk (Enterprise Security) search head. Make sure to
name it TA-windns otherwise ES won't eat it. 

## Configuration

This TA expects Windows DNS logging to be sourcetyped as `windns`. If you use a
different sourcetype, you should change `props.conf` accordingly in this TA.

## Life of a query

```
4/21/2016 8:35:27 AM 0A4C PACKET 000000B0CB13CB50 UDP Rcv 172.16.32.215 50eb Q [0001 D NOERROR] A (3)www(8)nanowolk(2)nl(0)
4/21/2016 8:35:27 AM 0A4C PACKET 000000B0CAAE2BE0 UDP Snd 172.16.32.254 a12d Q [0001 D NOERROR] A (3)www(8)nanowolk(2)nl(0)
4/21/2016 8:35:27 AM 0A4C PACKET 000000B0CA6377A0 UDP Rcv 172.16.32.254 a12d R Q [8081 DR NOERROR] A (3)www(8)nanowolk(2)nl(0)
4/21/2016 8:35:27 AM 0A4C PACKET 000000B0CB13CB50 UDP Snd 172.16.32.215 50eb R Q [8081 DR NOERROR] A (3)www(8)nanowolk(2)nl(0)

```

