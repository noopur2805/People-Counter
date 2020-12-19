# People-Counter

This project intends to count the number of people occupying multiple tables at any point of time.

- Obtained vanishing points using 3-line RANSAC, which were then used to change
perspective, so as to obtain bird eyes’s view.
- Using the transformation matrix obtained above, transformed polygon areas of a chair and a
person. If their overlap was above 50% threshold, then the seat is occupied, and the counter
of the occupancy at that table is incremented.
- To eliminate false positives (in case of people leaning on a table or standing nearby it),
height of a person is recorded while he enters the room, and is used to determine his pose
(standing or sitting).
