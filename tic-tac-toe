#include <vector>
#include <iostream>

using namespace std;


/// @brief Draws the provided tic-tac-toe board to the screen
//  @param board is the tic-tac-toe board that should be drawn
void drawBoard(const vector < char >&gameBoard) {
   for (int i = 0; i < 9; i += 3) {
      cout << "  " << gameBoard.at(i) << "  |  " << gameBoard.at(i + 1) << "  |  "
         << gameBoard.at(i + 2) << "  " << endl;
      if (i < 6) {
         cout << "-----|-----|-----" << endl;
      }
   }
   cout << endl;
    
   return;
}



/// @brief Fills vector with characters starting at lower case a.
///
///     If the vector is size 2 then it will have characters a to b.
///     If the vector is size 6 then it will have characters a to f.
///     If the vector is size 26 then it will have characters a to z.
///
/// @param v the vector to initialize
/// @pre-condition the vector size will never be over 26
void initVector(vector <char> &v) {
   vector<char> alphabet{'a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z'};
   
   for (int i = 0; i < v.size(); ++i) {
      v.at(i) = alphabet.at(i);
   }
   // TODO: implement function
   return;
}


/// @brief Converts a character representing a cell to associated vector index
/// @param the position to be converted to a vector index
/// @return the integer index in the vector, should be 0 to (vector size - 1)
int convertPosition(char boardPosition) {
   vector<char> alphabet{'a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z'};
   
   for (int i = 0; i < alphabet.size(); ++i) {
      if (alphabet.at(i) == boardPosition) {
         return i;
      }
   }
}


/// @brief Predicate function to determine if a spot in board is available.
/// @param board the current tic-tac-toe board 
/// @param position is an index into vector to check if available
/// @return true if position's state is available (not marked) AND is in bounds
bool validPlacement(const vector<char>  &gameBoard, int positionIndex) {
   if (positionIndex> -1 && positionIndex < 9) {
      if (gameBoard.at(positionIndex) != 'X' && gameBoard.at(positionIndex) != 'O') {
         return true;
      }
      else {
         return false;
      }
   }
   else {
      return false;
   }
   
   
}

/// @brief Acquires a play from the user as to where to put her mark
///
///     Utilizes convertPosition and validPlacement functions to convert the
///     user input and then determine if the converted input is a valid play.
///     Continues asking for a position until a valid position has been entered.
///
/// @param board the current tic-tac-toe board 
/// @return an integer index in board vector of a chosen available board spot
int getPlay(const vector<char> &gameBoard) {
   
   char boardPosition = ' ';
   cout << "Please choose a position: " << endl;
   cin >> boardPosition;
   bool isValid = false;
   while (!isValid) {
      int convertedInput = convertPosition(boardPosition);
      bool isValid = validPlacement(gameBoard, convertedInput);
      
      if (isValid) {
         return convertedInput;
      }
      else {
         cout << "Please choose a position: " << endl;
         cin >> boardPosition;
      }
   }
}


/// @brief Predicate function to determine if the game has been won
/// @param board the current tic-tac-toe board 
/// @return true if the game has been won, false otherwise
bool gameWon(const vector<char> &gameBoard) {
   bool gameOver = false;
   //   ***PLAYER 1 WIN CONDITIONS***
   if (gameBoard.at(0) == 'X' && gameBoard.at(1) == 'X' && gameBoard.at(2) == 'X') {
      gameOver = true;
   }
   else if (gameBoard.at(3) == 'X' && gameBoard.at(4) == 'X' && gameBoard.at(5) == 'X') {
      gameOver = true;
   }
   else if (gameBoard.at(6) == 'X' && gameBoard.at(7) == 'X' && gameBoard.at(8) == 'X') {
      gameOver = true;
   }
   
   else if (gameBoard.at(0) == 'X' && gameBoard.at(3) == 'X' && gameBoard.at(6) == 'X') {
      gameOver = true;
   }
   else if (gameBoard.at(1) == 'X' && gameBoard.at(4) == 'X' && gameBoard.at(7) == 'X') {
      gameOver = true;
   }
   else if (gameBoard.at(2) == 'X' && gameBoard.at(5) == 'X' && gameBoard.at(8) == 'X') {
      gameOver = true;
   }
   
   else if (gameBoard.at(0) == 'X' && gameBoard.at(4) == 'X' && gameBoard.at(8) == 'X') {
      gameOver = true;
   }
   else if (gameBoard.at(2) == 'X' && gameBoard.at(4) == 'X' && gameBoard.at(6) == 'X') {
      gameOver = true;
   }
   
   //   ***PLAYER 2 WIN CONDITIONS***
   else if (gameBoard.at(0) == 'O' && gameBoard.at(1) == 'O' && gameBoard.at(2) == 'O') {
      gameOver = true;
   }
   else if (gameBoard.at(3) == 'O' && gameBoard.at(4) == 'O' && gameBoard.at(5) == 'O') {
      gameOver = true;
   }
   else if (gameBoard.at(6) == 'O' && gameBoard.at(7) == 'O' && gameBoard.at(8) == 'O') {
      gameOver = true;
   }
   
   else if (gameBoard.at(0) == 'O' && gameBoard.at(3) == 'O' && gameBoard.at(6) == 'O') {
      gameOver = true;
   }
   else if (gameBoard.at(1) == 'O' && gameBoard.at(4) == 'O' && gameBoard.at(7) == 'O') {
      gameOver = true;
   }
   else if (gameBoard.at(2) == 'O' && gameBoard.at(5) == 'O' && gameBoard.at(8) == 'O') {
      gameOver = true;
   }
   
   else if (gameBoard.at(0) == 'O' && gameBoard.at(4) == 'O' && gameBoard.at(8) == 'O') {
      gameOver = true;
   }
   else if (gameBoard.at(2) == 'O' && gameBoard.at(4) == 'O' && gameBoard.at(6) == 'O') {
      gameOver = true;
   }
   
   return gameOver;
}


/// @brief Predicate function to determine if the board is full
/// @param board the current tic-tac-toe board 
/// @return true iff the board is full (no cell is available)
bool boardFull(const vector<char> &gameBoard) {
   bool isFull = false;
   int numMoves = 0;
   
   for (int i = 0; i < gameBoard.size(); ++i) {
      if (gameBoard.at(i) == 'X' || gameBoard.at(i) == 'O') {
         ++numMoves;
      }
   }
   
   if (numMoves == 9) {
      isFull = true;
   }

   return isFull;
}

const int PLAYER1 = 0;
const int PLAYER2 = 1;

int main() {
   vector<char> gameBoard(9);
   int curPlay;
   int whosTurn = PLAYER1; // Player 1 always goes first and is 'X'

   initVector(gameBoard);

   drawBoard(gameBoard);

   while (!gameWon(gameBoard) && !boardFull(gameBoard)) {
      
      curPlay = getPlay(gameBoard);

      if (whosTurn == PLAYER1) {
         gameBoard.at(curPlay) = 'X';

         whosTurn = PLAYER2;
      }
      else if (whosTurn == PLAYER2) {
         gameBoard.at(curPlay) = 'O';
         whosTurn = PLAYER1;
      }
      drawBoard(gameBoard);
      cout << endl;
   }

   if (boardFull(gameBoard)) {
      cout << "No one wins" << endl;
   }
   else if (whosTurn == PLAYER2) {
      cout << "Player 1 Wins!!" << endl;
   }
   else if (whosTurn == PLAYER1) {
      cout << "Player 2 Wins!!" << endl;
   }
   

   return 0;
}