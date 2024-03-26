In the initial days the one topic that troubled me most while learning react was the difference between a component and a function in react. So in this thread I will try my best to explain the difference to you between a react component and a function

A function is a piece of code that is created so that it can be reused again and again and we don't have to write same logic again and again at different places throughout our code. 
A component is also a piece of code that that is created so that it can be reused again anf again and we don't have to write the same logic again and again at different places but there is a difference --> A component is a part of the react core features (if a piece of code that you are reusing again and again is using react features like hooks (useState,useEffect etc.) than it is a component). For eg- If you are writing code for creating a user profile than you will be creating a component that will be used to display the profile of an user than you will be using that component again and again.
Let's take an example  -->

function sum(a,b) {
    return a +b;
    
}
The above mentioned example is a function as it does not involve react specific stuff.

function Sum(a,b){
    const [number,setNumber] = useState(1)     //Using this hook in this function will turn this function into a component.
    return(
        <div>
        {number}
        </div>
    )
}
In short if you have a reusable piece of code that has react superpowers inside it (useState,useEffect etc.) than it's a component.

So next time if you get stuck with this question that whether it's a component or a function simply ask yourself -->
Is this reusable piece of code has react stuff inside it or not
Some other facts -->
1. The name of the component generally starts with a capital letter, not a requirement but it' a convention
2. Component is a subset of function.

