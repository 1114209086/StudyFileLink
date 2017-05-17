# StudyFileLink
[Ant指南](http://www.cnblogs.com/hoojo/archive/2013/06/14/java_ant_project_target_task_run.html)  
[Markdown语法](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
[Markdown语法](https://segmentfault.com/markdown)

###一个ant的 build.xml
```xml
<?xml version="1.0"?>
<project name="Demo" default="run" basedir=".">
    <echo  message="import libs" />
    <path id="run.classpath">
        <fileset dir="${basedir}">
            <include name="lib/testng.jar" />
            <include name="lib/sikuli-script.jar" />
        </fileset>
        <fileset dir="${basedir}/lib/selenium">
            <include name="selenium-java-2.45.0.jar" />
            <include name="libs/*.jar" />
        </fileset>
    </path>
    <taskdef name="testng" classname="org.testng.TestNGAntTask" classpathref="run.classpath" />
    <target name="clean">
        <delete dir="build"/>
    </target>
    <target name="compile" depends="clean">
        <echo message="mkdir"/>
        <mkdir dir="build/classes"/>
        <javac srcdir="src" destdir="build/classes" debug="on" encoding="UTF-8">
            <classpath refid="run.classpath"/>
        </javac>
    </target>
    <path id="runpath"> 
         <path refid="run.classpath"/> 
         <pathelement location="build/classes"/> 
       </path> 
    <target name="run" depends="compile">
        <testng  classpathref="runpath"  outputDir="test-output">
            <xmlfileset dir="${basedir}" includes="testng.xml"/>
            <jvmarg value="-ea" />
        </testng>
    </target>
</project>
```
