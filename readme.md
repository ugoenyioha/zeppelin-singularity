# Zeppelin Singularity 🎈

A limited, single-node deployment of [Apache Zeppelin](http://zeppelin.incubator.apache.org) notebooks for [Apache Spark](http://spark.apache.org/) and PostgreSQL.

This app layers [zeppelin-in-space](https://github.com/heroku/zeppelin-in-space) on [spark-singularity](https://github.com/heroku/spark-singularity) to support limited, proof-of-concept experimentation using a single Heroku dyno in the [Common Runtime](https://devcenter.heroku.com/articles/dyno-runtime#common-runtime).

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/heroku/zeppelin-singularity)

## A few important notes 🌻

* [Performance-L dyno](https://www.heroku.com/pricing) is required to avoid memory errors
  * true big-data capabilities require a [Spark cluster](https://github.com/heroku/spark-in-space)
  * this single-instance deployment is suited for collaborative exploration & learning
* the settings found in Zeppelin UI: **Interpreter**, **Credential**, & **Configuration** are **read only**
  * change those settings by deploying from source with revisions to [`conf/interpreter.json.erb`](conf/interpreter.json.erb) & [`conf/zeppelin-site.xml`](conf/zeppelin-site.xml)
