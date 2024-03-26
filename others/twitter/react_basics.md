Naval Ravikant puts a lot of emphasis of Principles and I also believe the same. 
So today my objective is to make you understand what the hell is state in react-->

Before understanding state let us understand what is the problem that state is solving with the help of a story ?
React it is like a terminator it is super powerful but it has two very big weaknesses -->
 
1.It does only what you tell it do nothing less and nothing more 
2. Once you restart it, it forgets everything, it has no memory and relies totally on you.
Look at the following code snippet -->
Code snippet 
According to common sense the count should increase on button press but nothing is happening.
Reason -->
1. You are instructing react to increase the count of number  but you are nowhere mentioning that react should restart and  redraw the screen on number increase and react does only what you tell it nothing less and nothing more.
2. Even if you somehow tell react to repaint the screen still number will not increase because of the second weakness on restart it forgets everything it will forget your command that you wish to update the number and again nothing will happen.

So to counter this weakness we have state in react
State is the memory of react it will help us in the following ways -->
1. We will be telling react to restart and redraw iteslf on button click.
2. We will be giving a working memory to react using state so it remembers what it has to do after restarting.

Look at the example below --->

Now our code will work as expected 

Let us go more deep -->
State here has three parts
const [number,setNumber] = useState(0)
number ---> It is the what is stored in the memory of react here.
setNumber ---> It is used to set the memory of react.
0 ---> This is what initial value of the memory of react.

useState is a react hook and if you don't know what a hook is than --> click here.




