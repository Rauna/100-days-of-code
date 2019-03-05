# 100 Days Of Code - Log

### Day 32: 5th March 2019


**Today's Progress**: I worked on my Todo list app and also familiarised myself with git commands and pushed my Todo list code to GitHub. The app is still not complete and will be working on it.

**Thoughts:** I completed the delete functionality on this app which lets us delete the task once finished. While implementing the delete functionality, I was stuck at an error : **_'Uncaught TypeError: Cannot read property 'removeChild' of null'_**. Though the child element was getting removed, seeing this error on console was something that cannot be ignored. So, I searched for similar kind of an issue on stackoverflow and came across this question: 
https://stackoverflow.com/questions/39091505/i-receive-a-uncaught-typeerror-cannot-read-property-removechild-of-null-err

It was coming because of a for loop that created multiple event listeners for a particular element and even after the element was removed, the remaining instances of the events were trying to remove the element which was already removed, hence the error.

```the root of the problem is that you're calling thaticon(e) every time you add a list item, which means you're adding a new event listener every time it runs that loop. When you click the remove button It deletes the element the first time, then returns an error when it tries again and it doesn't exist. (Look at your for loop - if you add multiple Event Listeners they will stack).```

**Link to work:** [Todo list](https://github.com/RaunaqChawhan/Todo-List)
