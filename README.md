# chessboard-detection
**Automatic detection and classification of chess boards using CNN's**.

The synthetic dataset used for this project was generated with Blender and contains images of chessboards taken from an acute angle.
The objective of the project is to obtain the game state of the board in *FEN* notation, which is a compact way of representing chess game states.
The model has three steps:
* Board detection: using classical CV and ML algorithms, the $4$ corners of the chessboard are detected (the corners define the grid via a homography).
* Occupancy detection: each of the $64$ squares on the board is classified as occupied or empty using a fine-tuned ResNet18.
* Piece classification: the squares previously classified as occupied are classified by piece and color with a fine-tuned ResNet18.

Excellent results were obtained with all chessboards in the test set classified with $\leq 1$ error and $98$% of them classified perfectly.
