#!/bin/bash
board()
{
n=101
declare -A array
for(( i=0;i<10;i++ ))
do
if(( $i%2==0 ))
then
for((j=0;j<10;j++))
do
n=$(($n-1))
array[$i,$j]=$n
done
else
for((j=9;j>=0;j--))
do
n=$(($n-1))
array[$i,$j]=$n
done
fi
done
echo "________________________________________________________"
for((i=0;i<10;i++))
do
if(( $i==9 ))
then
for(( j=0; j<10; j++ ))
do
echo -n "| "
echo -n "${array[$i,$j]} |"
done
else
for(( j=0; j<10; j++ ))
do
echo -n "| "
echo -n "${array[$i,$j]} |"
done
fi
echo ""
echo "_________________________________________________________"
done
}
board

player1=0
echo "player1's intial position is:$player1 th position"


diceRoll=$(((RANDOM%6)+1))
echo "number appeared on Dice is :$diceRoll"


player1=0
playerCurrentPosition()
{
    value=$player1
#echo "player1's intial position is:$player1 th position"
    return $value
}

diceValue()
{
diceRoll=$(((RANDOM%6)+1))
#echo "number appeared on Dice is :$diceRoll"
    return $diceRoll
}

checkOption()
{
result=$((RANDOM%3))
if((result==0))
then
echo "No play"
echo "player1 is at position:$player1"

elif((result==1))
then
echo "Ladder"
diceValue
diceNumber=$?
playerCurrentPosition
position=$?
player1=$((position+diceNumber))
echo "player1 is at position:$player1"
else
echo "snake"
diceValue
diceNumber=$?
playerCurrentPosition
position=$?
player1=$((position-diceNumber))
echo "player1 is at position:$player1"
fi
}
checkOption
