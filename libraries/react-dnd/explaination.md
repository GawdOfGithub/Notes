####  Each todo is a draggable piece here which has it own index 

```jsx
   <Draggable
                  index={index}
                  key={todo.id}
                  draggableId={`${todo.id}`}
                >
                  {(draggableProvider) => (
                    <li
                      ref={draggableProvider.innerRef}
                      {...draggableProvider.draggableProps}
                      {...draggableProvider.dragHandleProps}
                    >
                      {todo.title}
                    </li>
                  )}
                </Draggable>
```

## The splice method -->
``` javascript
array.splice(start, deleteCount, item1, item2, ...);   
```
#### The splice method takes starting index as the first argument and number of elements to be removed as the second arguement and later #### areguements are the elemests that are to be added in the array if there is no deleteCount than the delete count will be 0 by default

```jsx
const handleDragEnd = (result) => {
    console.log(result)
    if(!result.destination) return; 
    const startIndex = result.source.index
    const endIndex = result.destination.index
    const copyTodos = [...todos]
    const [reorderTodo] = copyTodos.splice(startIndex,1)
    copyTodos.splice(endIndex,0,reorderTodo)   
    setTodos(copyTodos)
  }
  ```
  startIndex will be the index of todo that we are dragging from the source
  endIndex will be the index of the location where we want to drop that todo that we are dragging
  then we create a new array first we will add the original todos to the copyTodos then 

```javascript
 const [reorderTodo] = copyTodos.splice(startIndex,1)
```
Here we achieve two objectives at the same time first we remove the element as startIndex(source) from the copyTodos and then we add it to the reorderedTodo array and abstract the only element from the reorderedTodo that is the element that we removed from the copyTodos and in the next step we add the reorderedTodo to the endIndex(destination) of the copyTodos array and wallah we are done  