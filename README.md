Given the following, create and execute tests in `js-node`, `js-ie6`, `ruby2`, `python2`, `python3`, `java`, `objc-ios`, `objc-mac`, ...

```coffee
name: 'split'
args: [
  {name: 's',         type: 'unicode'}
  {name: 'delimiter', type: 'non-empty unicode'}
]
returns:              {type: 'unicode-list'}
code: {
  js:       's.split(delimiter)'
  ruby:     's.split(delimiter)'
  python:   's.split(delimiter)'
  java:     's.split(Pattern.quote(delimiter))'
  objc:     '[s componentsSeparatedByString:delimiter]'
}
unit_tests: [
  {args: ['a:b:c', ':'], result: ['a', 'b', 'c']}
  {args: ['foobar', 'ob'], result: ['fo', 'ar']}
  {args: ['a', ':'], result: ['a']}
  {args: ['a:', ':'], result: ['a', '']}
  {args: [':a', ':'], result: ['', 'a']}
  {args: ['', ':'], result: ['']}
  {args: [':', ':'], result: ['', '']}
]
```

### Status: just this README so far

### [License: MIT](LICENSE.txt)
