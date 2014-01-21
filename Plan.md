Jumper
==========
Set 3
1. getRow()
2. false
3. (4, 4)
4. Southeast
5. The parameters specify which location.

Set 4
1. getOccupiedAdjacentLocations(Location loc)
2. get(Location loc)
3. Grid has no code because it is an interface. The implementations of the methods are found in the AbstractGrid class.
4. It is better design to return the objects in an array list because one can change the array more easily. It can change to the addition of more actors or the deletion without a lot of implementation and coding.

Set 5
1. Location, Color, and Direction
2. Direction is North, color is blue.
3. It was created as a class because the actor has methods that the subclasses could inherit, and so we can create an actor object.
4. It cannot, object is already contained in grid. You can't remove it twice, because it is already gone the first time. You cannot put a bug in the grid, remove it, and put it back, because it won't be the same object.
5. The turn method used twice.

Set 6
1. Location next = loc.getAdjacentLocation(getDirection());
        if (!gr.isValid(next))
            return false;
2. Actor neighbor = gr.get(next);
        return (neighbor == null) || (neighbor instanceof Flower);
3. isValid(Location loc), so that the object can see if the adjacent locations are valid or not before moving to them.
	get(Location loc)
4. getAdjacentLocation(int direction)
5. getGrid();
	getLocation();
6. The method returns false, so the bug turns clockwise 45 degrees.
7. It is needed so that the method can use the getAdjacentLocation method later on.
8. The flower uses getColor(), which takes the color of the bug.
9. It doesn't.
10.Flower flower = new Flower(getColor());
   flower.putSelfInGrid(gr, loc);
11. 4 times

1) Specify
a. The jumper would turn and then jump.
b. It would turn until it could jump.
c. It would also turn and jump.
d. Turn and jump.
e. Turn until it is able to jump.
f. The jumper should be able to jump over and also land on a flower.

2) Design
a. Actor
b. Bug
c. Yes, there will be a constructor. Parameters specified could be location in the grid and color of the bug.
d. act
e. jump, canJump
f. Runner to run it
	Check ahead two spaces
	Check for the wall
	Check for other actors/objects
	Be able to jump two spaces ahead
	Be able to turn at a wall/obstruction until able to jump

