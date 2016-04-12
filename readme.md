### Run tests in WebStorm

    npm install
    npm run test
    
## Proposed change

Before

```
##teamcity[enteredTheMatrix]
##teamcity[testCount count='2']
##teamcity[testSuiteStarted nodeId='1' parentNodeId='0' name='Test suite' running='false' nodeType='suite' locationHint='suite://.../tests/test\.js.Test suite']
##teamcity[testStarted nodeId='2' parentNodeId='1' name='Should be skipped' running='false' nodeType='test' locationHint='test://.../tests/test\.js.Test suite.Should be skipped']
##teamcity[testStarted nodeId='3' parentNodeId='1' name='Should be skipped too' running='false' nodeType='test' locationHint='test://.../tests/test\.js.Test suite.Should be skipped too']
mocha-intellij: unexpectedly unprocessed element [object Object]##teamcity[testStarted nodeId='2' running='true']
##teamcity[testStarted nodeId='3' running='true']
##teamcity[testIgnored nodeId='2' message='Pending test |'Should be skipped|'']
##teamcity[testIgnored nodeId='3' message='Pending test |'Should be skipped too|'']
##teamcity[testSuiteFinished nodeId='1']
```

After

```
##teamcity[enteredTheMatrix]
##teamcity[testCount count='2']
##teamcity[testSuiteStarted nodeId='1' parentNodeId='0' name='Test suite' running='false' nodeType='suite' locationHint='suite://.../tests/test\.js.Test suite']
##teamcity[testStarted nodeId='2' parentNodeId='1' name='Should be skipped' running='false' nodeType='test' locationHint='test://.../tests/test\.js.Test suite.Should be skipped']
##teamcity[testStarted nodeId='3' parentNodeId='1' name='Should be skipped too' running='false' nodeType='test' locationHint='test://.../tests/test\.js.Test suite.Should be skipped too']
##teamcity[testStarted nodeId='2' running='true']
##teamcity[testIgnored nodeId='2' message='Pending test |'Should be skipped|'']
##teamcity[testStarted nodeId='3' running='true']
##teamcity[testIgnored nodeId='3' message='Pending test |'Should be skipped too|'']
##teamcity[testSuiteFinished nodeId='1']
```
