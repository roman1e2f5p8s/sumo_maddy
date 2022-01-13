1. Download map in format osm for the area of interest from www.openstreetmap.org (small areas) or extract.bbbike.org (large areas). Suppose you downloaded map.osm

2. Using netconvert (sumo.dlr.de/docs/netconvert.html), convert osm map to net.xml format which SUMO can read. At this stage, net.xml file can be opened with SUMO, but no simulations will be running.
Basic command to convert osm map: netconvert --osm-files map.osm --lefthand true -o map.net.xml

3. Random traffic can be generated with standard SUMO tool called randomTrips.py (https://sumo.dlr.de/docs/Tools/Trip.html)
Basic command to generate random routes: randomTrips.py --net-file map.net.xml --route-file routes.rou.xml --begin 0 --end 10000 --period 1

4. Create a SUMO configuration file scfg.sumocfg
