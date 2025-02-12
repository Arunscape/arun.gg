---
{"dg-publish":true,"permalink":"/programming/programming-concepts/google-next-2024-notes/"}
---


Google axion custom arm processor
Gemini 1.5 pro is huge, preview for developers now

Citadel talk:

Before:
generate p&l overnight for OTC price estimate 8 hours

They had a fixed worker pool, noisy neighbor problem (race condition, no resource isolation between jobs), it was on prem, no scaling

New system more failure tolerant


Problem: pod eviction/shuffling, they tightly packed pods into nodes and nodes into clusters

Cold start problem: create low priority pods in gke that real workers can quickly evict for resources. Heartbeat messages to keep it alive. They spin up entire nodes for jobs so they have placeholder small pods which are then evicted when a real job comes in


They created a backtesting on demand app from this


# AI in capital markets
Common theme: they likes the elastic scaling capabilities of moving to the cloud
### Cme group
The guys that manage risk
Started partnership when they needed to distribute realtime market data

Compute margin for 40billion portfolios
.5 million contracts available to search for a customer without having to download a local cache
Probability of fed monetary policy actions effect on interest rate available via API

Use AI to identify risk factors: try to generate them to predict future
Intelligent search engine for helping clients

Developer code assistant, focus on minimizing focus on details so developer scan integrate fast, working on the higher level details 

Was surprised: AI mostly a people problem not a technology problem. It changes how we work, how projects are organized 
Bets: more adoption of cloud. Interoperability of cloud platforms 
### Schwab
Started with Chatbot, dialogflow

Their focus is using AI to try and improve client experience 
Thinkorswim: AI research capabilities 
AI to figure out what equities align with certain themes for customers. E.g. ESG
40 million clients 9trillion client assets

Employee productivity: support desk summaries of clients

Read a bunch of scientific papers, ingest it with AI, find and surface outliers for the research people at Citadel
More info, more space to explore, less constraints for a given problem so can find better local minimums

Surprise: focus on speed for migrating TD Ameritrade customers to Schwab , speed for coming up with solutions 
Bets: AI risk management, what is the anthropological journey with AI gonna look like? 


### Citadel
Quantitative research 
They are very good at price discovery

Using AI to find patterns in data:
- unsupervised (the ai doesn't know what pattern you're looking for)
- supervised: give it some help, historical data
- data changes: future estimate changes, need to compute again 
- it's just another tool for them, a tool to enhance what they can do
- not looking to replace people /researchers
- 

Surprise: is cloud the natural of unnatural way of computing? He thinks cloud is the natural way, that's how it started out: centralized compute. Computing changed, personal devices much more powerful, cheaper to compute locally. Now we're back full circle, cloud is the way and cloud can be cheaper because of scaling 
 Ai is natural evolution: another tool for us just like books , calculators. 
Bets:


# AI for banking

### Macquarie 
2014 started migration to cloud
Differentiation for them for digital and data
Anything the customer sees is in gcp
Obviously using AI in non customer facing stuff 
Like copilot but also 
- predicting customer cashflow 
- Customer can ask for a review if their rating on their mortgage has improved 
- additional context in customer statements
- customers can add photos, notes, add hashtags, etc to personalize their purchase history and remember what the transaction was for
- manage risk
- 
### Scotiabank 
7 years ago
Data so "secure" that even the end user couldn't use it
"Been doing AI for a long time"
- 100s of models in production 
- data in cloud makes data scientists more productive 
- gen AI: solved one of their problems: business ownership of data quality
- easy to access
- AI on top of your knowledge base
- **knowledge base got way better because the data was more accessible and people actually went and updated out of date and incorrect data. It enabled a culture change, people participate in improving knowledgebase** not at all because of improvements in AI , the input data for way better because people actually used it
- 

### Intesa


### Discover
- framework to analyze risk
- legal team, other teams use it
- digital banking made customer service more difficult 
- only difficult questions surface because no need to call for balance anymore. Easy stuff is handled by the app
- being on hold = bad
- agent is searching for documents, gathering context 
- summarization makes this easier for the frontline agents
- AI feedback on what is a good response and a bad response for what to say to a customer
- assist technical writers for writing procedures for the agents to follow
- still goes through same review process as a normal human generated writing
- cut service time by 70%: minutes vs seconds, no need to be on hold 
- direct links to documents in the summary provided by AI


Common themes:
Engaging multiple teams : developers, legal, customer 

# Charles Schwab observability transformation
Client authentication: one login for all their products. Looks like their login application is developed in-house
- real time data observability (30-60 seconds)
- centralized observability data 
- usual elastic close scaling stuff
- single place for all logging, metrics and alerts

Before: siloed with many different observability tools. No connection between onsite and cloud stuff


Chaos testing, game days: practice outages
First hand experience how to handle things before a real outage happens
Gamified 

They used to not do any changes during market hours
After migration they lost control of that but they monitor the parts that can fail during market hours heavily


Bigquery optimization 


# accelerate open models with pytorch
Pytorch xla works on cpu GPU and tpu