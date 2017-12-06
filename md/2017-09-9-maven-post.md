---
layout: post
title: Maven学习
excerpt: "Maven学习"
categories: [study]
---
##Maven学习

2017-11-30
#打包spring boot项目jar maven-resources xxx类找到,需加入下面的依赖
		<plugin>
          <groupId>org.apache.maven.plugins</groupId>
          <artifactId>maven-resources-plugin</artifactId>
          <version>2.7</version><!--$NO-MVN-MAN-VER$ -->
        </plugin>
