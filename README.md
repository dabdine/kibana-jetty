kibana-jetty
============

[Kibana](http://www.elasticsearch.org/overview/kibana/) is a web-based search and filtering UI that sits on top of [Elasticsearch](http://www.elasticsearch.org/). This project contains a simple pom file that will download and unpack Kibana, then wrap it in a war and deploy it to jetty with the maven cargo plugin.

Disclaimer: I am not affiliated with elasticsearch in any way. I did this on my own accord to quickly get a server online without having to download / configure other tools or make a mess about my machine. *This* code is MIT-licensed though Kibana has its own license. See the Kibana license from Elasticsearch for more details.

For simple execution (defaults to es @ window.location & kibana version defined in pom.xml):

    mvn clean package cargo:run

To specify a specific Kibana location:

    mvn clean package cargo:run -Delasticsearch.location=http://xxx:port 

To specify a different Kibana version (for example, 3.1.0):

    mvn clean package cargo:run -Dkibana.version=3.1.0

Then access the kibana console from [http://localhost:8080/kibana](http://localhost:8080/kibana)

Build prerequisites
=============
1. JDK (6+ preferred, though I see no reason why this wouldn't work with v5)
2. Maven 2+

License
=======

The MIT License (MIT)

Copyright (c) 2013 Derek Abdine

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
