### You may wonder, now what the hell is request waterfall and why you should know about them??
##### Definition of Request Waterfall according to next docs->
###### A "waterfall" refers to a sequence of network requests that depend on the completion of previous requests. In the case of data fetching, each request can only begin once the previous request has returned data.
##### Basically it means that one async request will be processed only after the completion of previous one.For eg-->
```javascript
const result1 = await User_has_ordered_samosa()
const result2 = await User_is_eating_samosa() 
```
#### Here User_is_eating_samosa will execute only after the execution of User_has_ordered_samosa, and it makes complete sense as user will eat samosa only after he has ordered it

#### But now imagine a different set of requests
```javascript
const result1 = await User_has_ordered_pizza()
const result2 = await User_has_ordered_samosa()
```
#### Here user_has_ordered_samosa will execute only after user_has_ordered_pizza has finished executing , but we don't want this kind of behaviour as both samosa and pizza can be ordered at the same time thus saving time so to solve this isssue we will use hero of our story that is ##Promise.all command 
```javascript
 const data = await Promise.all([
      User_has_ordered_samosa,
      User_has_ordered_pizza
    ]);
```
### when we use Promise.all in javascript than all the promises under promise.all start resolving at the same time (samosa and pizza will be ordered at the same time thus saving precious time)