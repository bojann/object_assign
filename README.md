# object_assign
custom made Object.assign
```
const assigner = ( currObj={}, ...arrOfObjs ) => {
    try {
        if( arrOfObjs.length === 0 ) { 
            throw new Error("Enter sourceObject/'s that you want to copy");
        }

        for( let i=0; i<arrOfObjs.length; i++ ) {
            for( let key in arrOfObjs[i] ) {
                if( !(key in currObj) && arrOfObjs[i].hasOwnProperty(key) ) {
                    currObj[key] = arrOfObjs[i][key];
                }
            }
        }

        return currObj;
    } catch(err) {
		console.error(err)
	}
};
```
