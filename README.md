# junitnunitxsl

This stylesheet transforms a junit format unit test report into an nunit format.

While doing so, any text found within the test case name that is enclosed in square brackets is transfered into the test category node of the nunit report for that test.



Sample input

```
<testcase name="[SPK-499] Given silkBgOffsetStyle(silkUrl, index, totalSilks) is called When silkUrl is SPRITE-130x130.png Then it will return Object" time="0" classname="Then it will return Object">
</testcase>
```


Sample output
```
<test-case name="Given silkBgOffsetStyle(silkUrl, index, totalSilks) is called When silkUrl is SPRITE-130x130.png Then it will return Object"
            description="Then it will return Object"
            success="True"
            time="0"
            executed="True"
            asserts="1"
            result="Success">
    <categories>
       <category name="S"/>
       <category name="SPK-499"/>
    </categories>
 </test-case>	
```
