# Eclipse Errors : Maven Related

## Errors

---

### **Could not calculate build plan: Plugin org.apache.maven.plugins:maven-war-plugin:2**

#### *Solution*

[Source][1]

1. Delete m2e-lastUpdated.properties

    - Default path: C:\Users\\*user*\.me\repository\org\apache\maven\plugins\maven-war-plugin\2.2

2. In eclipse, right click project > Run as > Maven clean

3. In eclipse, right click project > Run as > Maven install

4. In eclipse, right click project > Maven > Update Project
5. Refresh project

[1]: https://dotblogs.com.tw/grayyin/2019/09/17/192207

---

### **org.apache.maven.archiver.MavenArchiver.getManifest**

*Root cause*

The version of the *maven-jar-plugin* in the project pom.xml is not match with the version of maven.

*Solution*

Solution A

> Right click > Maven > Update Project

Solution B

Update Eclipse m2e extensions

1. Help > Install New Software

2. Add/Edit with following:
    - name: m2e
    - url: http://repo1.maven.org/maven2/.m2e/connectors/m2eclipse-mavenarchiver/0,17.2/N/LATEST/

3. Select and update

4. Right click project > Maven > Update Project

*Workaround*

Replace the version of the *maven-jar-plugin* denoted in the pom.xml with version 2.6

Example: pom.xml with *maven-jar-plugin* ver 3.0.2

    <plugin>
        <artifcatId>maven-jar-plugin</artifactId>
        <version>3.0.2</version>
    <plugin>

change to version 2.6

    <plugin>
        <artifcatId>maven-jar-plugin</artifactId>
        <version>2.6</version>
    <plugin>