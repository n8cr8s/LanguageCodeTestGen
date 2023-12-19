# Language, Function and a test

## Description

This file contains code to define functions for a given language and create a test for the created code.

## Requirements

Python 3.10 or Greater
Go to https://openai.com, create an account.
- Click on API
- Click on Settings, add payment information.
- Click on API keys.
- Generate an API KEY and copy it down in a safe and secure place.  It is a best practice to use separate API keys for test and production.

## Usage

Set the OPENAPI_KEY to the value above.  Then run the application. 

Execute the following commands:
```
export OPENAPI_KEY=<OPEN API KEY>
python main.py 
```

### Optional Arguments

--language <language> 
--task '<description of function desired>'

Example
```
python main.py --language javascript --task 'return the sum of an array of numbers'
```

Output
```
{'language': 'javascript', 'task': 'return the sum of an array of numbers', 'test': "\n\ndescribe('sumArray', () => {\n  it('returns the sum of an array of numbers', () => {\n    const numbers = [1,2,3,4,5];\n    const expectedSum = 15;\n    expect(sumArray(numbers)).toEqual(expectedSum);\n  });\n});", 'code': '\n\nfunction sumArray(arr) {\n  return arr.reduce((a, b) => a + b, 0);\n}'}
```