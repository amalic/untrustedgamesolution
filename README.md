<h2>Game: <a href="http://alexnisnevich.github.io/untrusted/">http://alexnisnevich.github.io/untrusted/</a></h2>

<h3>Level 01</h3>
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

<h3>Level 02</h3>
```javascript
	maze = new ROT.Map.DividedMaze(3,3);
```
```javascript
	map.placeObject(8, 5, 'exit');
```

<h3>Level 03</h3>
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

<h3>Level 04</h3>
```javascript
    map.placeObject(map.getWidth()-4, map.getHeight()-4, 'exit')
```

<h3>Level 05</h3>
```javascript
			map.setSquareColor(x, y, '#0f0');
```

<h3>Level 06</h3>
```javascript
        
	function moveToward(obj, type) {
        var target = obj.findNearest('exit');
        var leftDist = obj.getX() ;
        var upDist = obj.getY() - target.y;
        
        var direction;
        if (upDist == 0 && leftDist == 0) {
        	return;
        } if (upDist > 0 && upDist >= leftDist) {
            direction = 'up';
        } else if (upDist < 0 && upDist < leftDist) {
            direction = 'down';
        } else if (leftDist > 0 && leftDist >= upDist) {
            direction = 'left';
        } else {
            direction = 'right';
        }
        
        if (obj.canMove(direction)) {
            obj.move(direction);
        }
    }
```

<h3>Level 07</h3>
```javascript
        var player = map.getPlayer();
        
        if(player.getColor() == '#ff0')
        	player.setColor('#0f0');
        else if(player.getColor() == '#0f0')
        	player.setColor('#f00');
        else if(player.getColor() == '#f00')
        	player.setColor('#ff0');
```

<h3>Level 08</h3>
```javascript
"generateForest"
```

<h3>Level 09</h3>
```javascript
    player.setPhoneCallback(function(){
    	if(raftDirection == 'down')
   			raftDirection = 'up';
        else
        	raftDirection = 'down';
    });
```

<h3>Level 10</h3>
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

<h3>Level 11</h3>
```javascript
            // Available commands: me.move(direction)
            //                 and me.canMove(direction)
            if(me.canMove('right'))
            	me.move('right')
            else if(me.canMove('down'))
            	me.move('down');
```

<h3>Level 12</h3>
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

<h3>Level 13</h3>
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

<h3>Level 14</h3>
```javascript
'greenKey');map.placeObject(24,10,'greenKey'
```

<h3>Level 15</h3>
```javascript
()}, 'onCollision': function(player){//
```

<h3>Level 16</h3>
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

<h3>Level 17</h3>
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

<h3>Level 18</h3>
```javascript
 	}
    
	function gravity() {
```

<h3>Level 19</h3>
<pre>
Press 5 x UP, keep RIGHT button pressed until you reach next level
</pre>

<h3>Level 20</h3>
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

<h3>Level 21</h3>
Menu --> scripts/objects.js -> Line 92
```javascript
                //if (!game.map.finalLevel) {
                    game._moveToNextLevel();
                //}
```
