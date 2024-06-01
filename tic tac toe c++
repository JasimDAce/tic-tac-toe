#include<iostream> 
using namespace std;


char square[] = {'0','1','2','3','4','5','6','7','8','9'};

void board(){
    cout << "\n\n\tWELCOME MY SON!! WELCOME TO THE GAME!!\n\n";
    cout << "\t\tTIC TAC TOE\n\n";
    cout << "\tPLAYER 1 - X       PLAYER 2 - O\n\n\n";
    
    cout << "\t\t     |     |     \n";
    cout << "\t\t  "<<square[1]<<"  |  "<<square[2]<<"  |  "<<square[3]<<"  \n";
    cout << "\t\t_____|_____|_____\n";
    cout << "\t\t     |     |     \n";
    cout << "\t\t  "<<square[4]<<"  |  "<<square[5]<<"  |  "<<square[6]<<"  \n";
    cout << "\t\t_____|_____|_____\n";
    cout << "\t\t     |     |     \n";
    cout << "\t\t  "<<square[7]<<"  |  "<<square[8]<<"  |  "<<square[9]<<"  \n";
    cout << "\t\t     |     |     \n";
}

int check(){
    if(square[1] == square[2] && square[2] == square[3])
        return 1;
    else if(square[4] == square[5] && square[5] == square[6])
        return 1;
    else if(square[7] == square[8] && square[8] == square[9])
        return 1;
    else if(square[1] == square[4] && square[4] == square[7])
        return 1;
    else if(square[2] == square[5] && square[5] == square[8])
        return 1;
    else if(square[3] == square[6] && square[6] == square[9])
        return 1;
    else if(square[1] == square[5] && square[5] == square[9])
        return 1;
    else if(square[3] == square[5] && square[5] == square[7])
        return 1;
    else if(square[1] != '1' && square[2] != '2' && square[3] != '3' && square[4] != '4' && square[5] != '5' && square[6] != '6' && square[7] != '7' && square[8] != '8' && square[9] != '9')
        return 0;
    else
        return -1;
}

int main(){
    string player1;
    string player2;
    int currPlayer = 1;
    int move;
    char mark;
    int i;
    cout << "\n\n\tEnter your name Player 1 : ";
    cin >> player1;
    cout << "\n\n\tEnter your name Player 2 : ";
    cin >> player2;
    
    do{
        cout << "\x1B[2J\x1B[H";
        board();
        currPlayer = (currPlayer%2)?1:2;
        string name = (currPlayer == 1)?player1:player2;
        cout << "\n\tEnter your move " << name<< ": ";
        cin >> move;
        mark = (currPlayer == 1)?'X':'O';
        if(move == 1 && square[1] == '1')
            square[1] = mark;
        else if(move == 2 && square[2] == '2')
            square[2] = mark;
        else if(move == 3 && square[3] == '3')
            square[3] = mark;
        else if(move == 4 && square[4] == '4')
            square[4] = mark;
        else if(move == 5 && square[5] == '5')
            square[5] = mark;
        else if(move == 6 && square[6] == '6')
            square[6] = mark;
        else if(move == 7 && square[7] == '7')
            square[7] = mark;
        else if(move == 8 && square[8] == '8')
            square[8] = mark;
        else if(move == 9 && square[9] == '9')
            square[9] = mark;
        else{
            currPlayer--;
            cout << "\nInvalid Move" << endl;
        }
        currPlayer++;
        i = check();
    }while(i == -1);
    cout << "\x1B[2J\x1B[H";
    board();
  if(i == 1){
      if(currPlayer == 2){
          cout << "\n\n\tWOHOOO!! YOU WON " << player1; 
      }
      else{
          cout << "\n\n\tWOHOOO!! YOU WON " << player2;
      }
  }  
  else{
      cout << "\n\n\tSUCKS!! ITS A DRAW";
  }
    return 0;
}
