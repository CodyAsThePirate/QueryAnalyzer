QueryAnalyzer
=============

Module that shows every executed query and the execution time.


##Setup
- Add "weteef/queryanalyzer": "1.*" to the require section of your composer.json
- Attach Profiler to your DB-Adapter.
$serviceManager->get('Zend\Db\Adapter\Adapter')->setProfiler(new \QueryAnalyzer\Db\Adapter\Profiler\QueryAnalyzerProfiler());

- If your DB Adapater does not have the name Zend\Db\Adapter\Adapter you need to create an alias in the config:
```
'aliases' => array(
    'Zend\Db\Adapter\Adapter' => 'your-db-adapter-name',
)
```

After these steps the analyzer should appear on the bottom right corner of your browser window.
