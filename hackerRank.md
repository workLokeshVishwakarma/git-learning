- [Data Finder](#data-finder)
- Account Transactions
- Joined Logger
- Strip Property
- Weekday Text
- Activity List
- Champions League Teams
- Image Cloning
- Parking Lot
- User Transactions
- Notes Store
- Staff List
- Employee Inheritance
- Last and Second-last
- Restocking the Warehouse
- Reductor Array

<hr />

### Order List Processing

```javascript
function processOrderList(orderList, orderId, state) {
  // Write your code here
  return state === 'Processing' ?
      orderList.map(item => ({
          ...item,
          state: item.id === orderId ? 'Processing' : item.state
      })) :
      orderList.filter(item => item.id !== orderId);
}
```


### Data Finder

```javascript
function dataFinder(data) {
    var find = function(minRange, maxRange, value) {
        if (minRange < 0 || maxRange >= data.length) {
            throw new Error('Invalid range');
        }
        for (let i = minRange; i <= maxRange; i++) {
            if (data[i] === value) {
                return true;
            }
        }
        return false;
    }
    return find;
}
```


### JavaScript Weekday Text

```javascript
function weekdayText(weekdays) {
    return function getText(target) {
        return weekdays[target] || (function () {
            throw new Error(`Invalid weekday number`)
        }());
    }
}
```


### Strip Property

```javascript
function stripProperty(obj, prop) {
   // write your code here
     delete obj[prop];
      return obj;
      return {};
}
```


### Notes Store

```javascript
const completedNotes = [];
const activeNotes = [];
const otherNotes = [];

class NotesStore {

    addNote(state, name) {
        if (name === undefined || name === null || name === '') {
            throw new Error('Name cannot be empty');
        }
        if (!this.isValid(state)) {
            throw new Error('Invalid state ' + state);
        }
        this.getNotesList(state).push(name);
    }

    getNotes(state) {
        if (!this.isValid(state)) {
            throw new Error('Invalid state ' + state);
        }
        return this.getNotesList(state);
    }

    getNotesList(state) {
        if (state === 'completed') {
            return completedNotes;
        } else if (state === 'active') {
            return activeNotes;
        }
        return otherNotes;
    }

    isValid(state) {
        return state === 'completed'
            || state === 'active'
            || state === 'others';
    }
}
```


### Step Counter

```javascript
function getFixedCounter(k) {
  // write your code here
  let myCounter = counter;
  return {
    increment: () => {
      myCounter.changeBy(k);
    },
    decrement: () => {
      myCounter.changeBy(-k);
    },
    getValue: () => {
      return myCounter.getValue();
    },
  };
}
```


### Fizz Buzz

```javascript
function  fizzBuzz(number) {
    for (let i = 1 ; i <= number ; i++) {
        if (i % 3 === 0 && i % 5 === 0) {
            console.log('FizzBuzz');
        } else if (i % 3 === 0) {
            console.log('Fizz');
        } else if (i % 5 === 0) {
            console.log('Buzz');
        } else {
            console.log(i);
        }
    }
}
```