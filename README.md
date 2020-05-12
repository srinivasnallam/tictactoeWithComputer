# tictactoeWithComputer
Code to play tic tac toe game with machine 


import random
myboard1={1:1,2:2,3:3,4:4,5:5,6:6,7:7,8:8,9:9}
a=1
def pri(board):
    print (1,2,3 ,sep='|')
    print('-','+','-','+','-',sep='')
    print(4,5,6,sep='|')
    print('-','+','-','+','-',sep='')
    print(7,8,9,sep='|')
    print('-','+','-','+','-',sep='')
    turn='x'
    for i in range(9):
        if (turn == 'x'):
            print("Now  its turn of "+turn+" which place do you want to move:")
        else :
            print('Now its my turn :)')
        if (turn == 'o'):
            mov = random.randint(1,9)
        else:
            mov=int(input())
        if board[mov] == 'x' or board[mov] == 'o':
            print('That position is already taken')
        else:
            board[mov]=turn
            print(board[1],board[2],board[3],sep='|')
            print('-','+','-','+','-',sep='')
            print(board[4],board[5],board[6],sep='|')
            print('-','+','-','+','-',sep='')
            print(board[7],board[8],board[9],sep='|')
            print('-','+','-','+','-',sep='')
            temboard=board
            print("--------------------------------------------------------------")
            if turn=='x':
                turn='o'
            else:
                turn='x'
            if  (board[1]==board[2] and board[2]==board[3] or
                board[1]==board[4] and board[4]==board[7] or
                board[7]==board[8] and board[8]==board[9] or
                board[3]==board[6] and board[6]==board[9] or
                board[4]==board[5]and board[5]==board[6]  or
                board[2]==board[5]and board[5]==board[8]  or
                board[1]==board[5]and board[5]==board[9] or
                board[3]==board[5]and board[5]==board[7]):
                print('Game over,And the winner is:')
                if turn=='x':
                    print('o')
                else:
                    print('x')
                print('Do you want to play another game(y/n):')
                b=input()
                if(b=='y'):
                    a=1
                else:
                    a=1
                break
if(a==1):
    pri(myboard1)
else:
    exit()
