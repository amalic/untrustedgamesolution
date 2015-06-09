<h2>Game: <a href="http://alexnisnevich.github.io/untrusted/">http://alexnisnevich.github.io/untrusted/</a></h2>

<ul>
<li><a href="#lvl01">Level 01</a></li>
<li><a href="#lvl02">Level 02</a></li>
<li><a href="#lvl03">Level 03</a></li>
<li><a href="#lvl04">Level 04</a></li>
<li><a href="#lvl05">Level 05</a></li>
<li><a href="#lvl06">Level 06</a></li>
<li><a href="#lvl07">Level 07</a></li>
<li><a href="#lvl08">Level 08</a></li>
<li><a href="#lvl09">Level 09</a></li>
<li><a href="#lvl10">Level 10</a></li>
<li><a href="#lvl11">Level 11</a></li>
<li><a href="#lvl12">Level 12</a></li>
<li><a href="#lvl13">Level 13</a></li>
<li><a href="#lvl14">Level 14</a></li>
<li><a href="#lvl15">Level 15</a></li>
<li><a href="#lvl16">Level 16</a></li>
<li><a href="#lvl17">Level 17</a></li>
<li><a href="#lvl18">Level 18</a></li>
<li><a href="#lvl19">Level 19</a></li>
<li><a href="#lvl20">Level 10</a></li>
<li><a href="#lvl21">Level 21</a></li>
</ul>

<a name="lvl01"><a name="lvl01"><h3>Level 01</h3></a>
```javascript
    //for (y = 3; y <= map.getHeight() - 10; y++) {
        //map.placeObject(5, y, 'block');
        //map.placeObject(map.getWidth() - 5, y, 'block');
    //}
    
    //for (x = 5; x <= map.getWidth() - 5; x++) {
        //map.placeObject(x, 3, 'block');
        //map.placeObject(x, map.getHeight() - 10, 'block');
    //}
    map.placeObject(8, 5, 'computer');
    map.placeObject(9, 5, 'exit');
```

<a name="lvl02"><h3>Level 02</h3></a>
```javascript
	maze = new ROT.Map.DividedMaze(1, 1);
```
```javascript
	map.placeObject(8, 5, 'exit');
```

<a name="lvl03"><h3>Level 03</h3></a>
```javascript
    for (y = 10; y <= map.getHeight() - 3; y++) {
        map.placeObject(map.getWidth() - 6, y, 'block');
        map.placeObject(map.getWidth() - 5, y, 'block');
    }
    
    for (x = 5; x <= map.getWidth() - 5; x++) {
        map.placeObject(x,  map.getHeight() - 4, 'block');
        map.placeObject(x, map.getHeight() - 3, 'block');
    }
```

<a name="lvl04"><h3>Level 04</h3></a>
```javascript
    map.placeObject(map.getWidth()-4, map.getHeight()-4, 'exit')
```

<a name="lvl05"><h3>Level 05</h3></a>
```javascript
			map.setSquareColor(x, y, '#0f0');
```

<a name="lvl06"><h3>Level 06</h3></a>
```javascript
    function moveToward(obj, type) {
        if(obj.canMove('left'))
            obj.move('left');
    }
```

<a name="lvl07"><h3>Level 07</h3></a>
```javascript
        var player = map.getPlayer();
        
        if(player.getColor() == '#ff0')
        	player.setColor('#0f0');
        else if(player.getColor() == '#0f0')
        	player.setColor('#f00');
        else if(player.getColor() == '#f00')
        	player.setColor('#ff0');
```

<a name="lvl08"><h3>Level 08</h3></a>
```javascript
"generateForest"
```

<a name="lvl09"><h3>Level 09</h3></a>
```javascript
    player.setPhoneCallback(function(){
    	if(raftDirection == 'down')
   			raftDirection = 'up';
        else
        	raftDirection = 'down';
    });
```

<a name="lvl10"><h3>Level 10</h3></a>
```javascript
            if(me.getY()==12)
            	me.move('left');
```
```javascript
			// nothing to do here;
```
```javascript
            if(me.getY()==12)
            	me.move('left')
```

<a name="lvl11"><h3>Level 11</h3></a>
```javascript
            // Available commands: me.move(direction)
            //                 and me.canMove(direction)
            if(me.canMove('right'))
            	me.move('right')
            else if(me.canMove('down'))
            	me.move('down');
```

<a name="lvl12"><h3>Level 12</h3></a>
```javascript
            var xDiff = me.getX() - player.getX();
            var yDiff = me.getY() - (map.getHeight() - player.getY());
            
            if(xDiff<0 && me.canMove('right'))
            	me.move('right');
            else if(xDiff>0 && me.canMove('left'))
            	me.move('left');
            else if(yDiff>0 && me.canMove('up'))
            	me.move('up');
            else if(yDiff<0 && me.canMove('down'))
            	me.move('down');
```

<a name="lvl13"><h3>Level 13</h3></a>
```javascript
            // move randomly
            //var moves = map.getAdjacentEmptyCells(me.getX(), me.getY());
            // getAdjacentEmptyCells gives array of ((x, y), direction) pairs
            //me.move(moves[map.getRandomInt(0, moves.length - 1)][1]);
            var xDiff = me.getX() - player.getX();
            var yDiff = me.getY() - (map.getHeight() - player.getY());
            
            if(xDiff<0 && me.canMove('right'))
            	me.move('right');
            else if(xDiff>0 && me.canMove('left'))
            	me.move('left');
            else if(yDiff>0 && me.canMove('up'))
            	me.move('up');
            else if(yDiff<0 && me.canMove('down'))
            	me.move('down');
```

<a name="lvl14"><h3>Level 14</h3></a>
```javascript
'greenKey');map.placeObject(24,10,'greenKey'
```

<a name="lvl15"><h3>Level 15</h3></a>
```javascript
()}, 'onCollision': function(player){//
```

<a name="lvl16"><h3>Level 16</h3></a>
```javascript
        // using canvas to draw the line
        var ctx = map.getCanvasContext();
        ctx.beginPath();
        ctx.strokeStyle = 'white';
        ctx.lineWidth = 5;
        ctx.moveTo(x1, y1);
        ctx.lineTo(x2, y2);
        ctx.stroke();
```
```javascript
	getRandomInt = function(a, b) {return 0;}
```

<a name="lvl17"><h3>Level 17</h3></a>
```javascript
        // TODO find a way to remove the API docs
        // wouldn't want the 'good doctor' to find
        // out about map.getCanvasCoords()...
    }
    
    var lt = teleportersAndTraps[0];
    for(i=teleportersAndTraps.length-1; i>=0; i--) {
    	var t = teleportersAndTraps[i];
    	if(t.getType() == 'teleporter')
        	if(lt.getY() <= t.getY() && lt.getX() < t.getX()) {
                	lt = t;
            }
            if(lt.getY()<t.getY()) {
            	lt = t;
            }
    }
    
    for (i = 0; i < teleportersAndTraps.length; i++) {
    	var t = teleportersAndTraps[i];
    	if(t.getType() == 'teleporter')
        	if(t != lt)
            	t.setTarget(lt);
```

<a name="lvl18"><h3>Level 18</h3></a>
```javascript
 	}
    
	function gravity() {
```

<a name="lvl19"><h3>Level 19</h3></a>
Press 5 x UP :fast_forward: keep RIGHT button pressed until you reach next level


<a name="lvl20"><h3>Level 20</h3></a>
```javascript
	map.placeObject(25, 22, 'block');
    
    map.defineObject('bossKiller', {
      'type': 'dynamic',
      'symbol': '*',
      'color': 'blue',
      'interval': 100,
      'projectile': true,
      'behavior': function (me) { 
        me.move('left');
      }
    });
        
    map.getPlayer().setPhoneCallback(function(){
    	var hero=map.getPlayer();
    	map.placeObject(hero.getX()-1, hero.getY(), 'bossKiller');
    });
```

<a name="lvl21"><h3>Level 21</h3></a>
Menu :fast_forward: scripts/objects.js :fast_forward: Line 92
```javascript
                //if (!game.map.finalLevel) {
                    game._moveToNextLevel();
                //}
```
