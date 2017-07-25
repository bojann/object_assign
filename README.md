# object_assign
custom made Object.assign
```
const assigner = ( currObj={}, ...arrOfObjs ) => {
    if( arrOfObjs.length === 0 ) { 
        console.log("Enter sourceObject/'s that you want to copy") ;
        return false;
    }

    for( let i=0; i<arrOfObjs.length; i++ ) {
        for( let key in arrOfObjs[i] ) {
            if( !(key in currObj) && arrOfObjs[i].hasOwnProperty(key) ) {
                currObj[key] = arrOfObjs[i][key];
            }
        }
    }

    return currObj;
};
```
