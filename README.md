# exception

## Error class with possible cause

- Class `Exception` is similar to java Exception class where you can pass cause error object to constructor.
```javascript
    try {
        // some code
    } catch (err) {
        throw new Exception ("Here is my exception with inner error", err);
    }
```
- This class has static method `Exception.errSerializer` which extracts data from provided Error object and returns a simple object ready for serialization.
Following fields are checked:
    - `name`
    - `message`
    - `code`
    - `signal`
    - `stack` - can be skipped if second parameter is set to false
    - `cause`
