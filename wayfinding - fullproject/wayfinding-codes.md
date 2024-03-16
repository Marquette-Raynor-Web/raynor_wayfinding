Line 337 - buildDataStore(mapNum, map, el))

// creating data from the svg maps provided

​        

Line 447 - function buildPortals() { 

// after data extracted from all svg maps then build portals between them





Line 545 - function getDoorPaths(door) {     **<--- i think this is the main culprit of where it all starts**

//get the set of paths adjacent to a door or endpoint.





**Line 575** - function recursiveSearch(segmentType, segmentFloor, segment, length) {





 Line 629 -  function generateRoutes() {





Line 711 - function build() {

​            dataStore = {

​                'p': [], // paths

​                'q': [] // portals

​            };

​            portalSegments = [];

​            // Build the dataStore from each map given

​            $.each(maps, function (i, map) {

​                // cleanupSVG(map.el); // commented out as already run by initialize

​                buildDataStore(i, map, map.el);

​            });

​            buildPortals();

​            generateRoutes();

​            return dataStore;

​        } // function build





