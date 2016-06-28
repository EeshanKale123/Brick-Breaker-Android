# Brick-Breaker-Android
Classic DX Ball

There are total of 3 lives. Issue with setting the initial position of the ball (starts always at x/2 and y/2 but pops up suddenly before the user has a chance to react). Need to always start ball on top of paddle (initial position). Sometimes, bad physics on the brick collision.

The main class is the GameView, which extends the SurfaceView(for touch events) and implements the Runnable interface(which is responsible for the threading)
The RectF class(thanks to kilobolt.com) was used to detect the collisions between the bricks and ball, and the ball and paddle. 
Since it was a native android class, the methods were very easy to use and provided efficient deetection.

Things that need updating :
1. Collision physics of the ball is not accurate (since very very basic math is used)
2. The paddle needs to reset if the ball goes below the paddle.
3. Game end condition (all bricks destroyed is not implemented). 
4. The ball should fall downwards relevant to paddles last position.
5. Possibility of implementing paddle movement using phone tilt by using Accelerometer and Magnetometer (under work)

The other classes are pretty self explanatory, which basically involve updating their states on canvas, or just for creation in their constructors.
