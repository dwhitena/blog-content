![](/content/images/2016/01/go-dashing.png)

About three or four months ago, I was approached by a client wanting a series of real-time dashboards reporting things like revenue, costs, customer usage, server usage, etc. with a granularity of seconds to minutes.  As such, I did quite a few POCs and eventual implementations of dashboards with a variety of technologies.  Some of these technologies were/are easier and/or more useful than others.

Before continuing, let me clarify what I mean when I'm referring to an "easy" or "useful" or "good" dashboard:

* A "good" dashboard should easily display a minimum amount of information needed to immediately ascertain the state of something (e.g., a server or company finances) without a lot of cluster, which just confuses the situation.
* An "easy" and "useful" dashboard should be built such that the target audience can  interact with the dashboard without a large learning curve.  The sophistication of these interactions and corresponding learning curves may differ greatly for different audiences (engineers vs. sales people).
* Furthermore, a dashboard meeting the above criteria should also be relatively quick to setup and maintain, because turns out there are other things that need to be done at tech companies.

For one these dashboards, I ended up using the [ELK](https://www.elastic.co/) stack.  Specifically, I utilized [Logstash](https://www.elastic.co/products/logstash) to push logged metrics into [Elasticsearch](https://www.elastic.co/products/elasticsearch) and [Kibana](https://www.elastic.co/products/kibana) for the dashboard.  This was good for the target audience of mostly engineers and support personal who could pick up the drill down operations and [Lucene](https://lucene.apache.org/core/2_9_4/queryparsersyntax.html) query language quickly.  However, for another dashboard for sales/marketing, this would not have proved to be an "easy" and "useful" solution.  The sales/marketing folks wanted something that would be real-time, but would also be more in-your-face about issues/events without having to query via some new language.

Enter [Go](https://golang.org/) and [Dashing](http://dashing.io/).  If you are not familiar, [Dashing](http://dashing.io/) is a "Sinatra based framework that lets you build beautiful dashboards."  It is open source (https://github.com/Shopify/dashing), was developed by [Shopify](https://www.shopify.com/), and has an active community developing tons of [third-party widgets](https://github.com/Shopify/dashing/wiki/Additional-Widgets).

[Go](https://golang.org/) may not be the first language that you think of when building a [Dashing](http://dashing.io/) dashboard, as many run [Ruby](https://www.ruby-lang.org/en/) jobs to populate the dashboards.  However, I will argue here that [Go](https://golang.org/) is a great choice, and has proved quite useful for me in combination with [Dashing](http://dashing.io/).

### Dashing setup

### Go job

### Deployment/use