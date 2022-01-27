# rexgen-nodejs-demo
Sample code for using ReXgen in Linux.

Usage:
node gnss2can.js can0
node gnss2can.js can1
node gnss2can.js myfile
node gnss2can.js > /path/to/output

canreader.js outputs data to default output - console (process.stdout)
It can be redirected using standard linux flow:
canreader.js > myfile


This line is sending gnss to rx fifo of rexgen, and simultaneously run canreader.js to output what is read.
node gnss2can.js > /var/run/rexgen/can0/rx & node canreader.js