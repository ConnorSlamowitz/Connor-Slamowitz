---
layout: post
title: 001 - NLP .pdf Highlighter
---
## PhD Productivity Hacking

I would consider myself a novice at programming. I have done courses in python, web development, database management, and object oriented programming, but I would
never really feel comfortable doing anything more than making pretty graphs with Plotly or organizing data with Pandas. However, I do often find myself lurking on
the [machine learning subreddit](http://www.reddit.com/r/machinelearning)to see what more talented programmers can do with modern architectures. It's actually pretty
cool to see the projects current ML researchers are working on. I have seen tools that can convert HD pictures into [Van Gogh paintings](https://towardsdatascience.com/style-transfer-with-gans-on-hd-images-88e8efcf3716), 
video processing applications that can [convert 15 FPS videos into 60 FPS videos](https://gigazine.net/gsc_news/en/20200121-dain-app/), and even applications that utilize
GPT-3 to [generate ideas for blogs](https://thenextweb.com/neural/2020/10/22/this-gpt-3-powered-tool-generates-new-ideas-for-your-terrible-blog/) (could this just be an instance
of auto-generated robot vomit?)  

Looking at these tools have thus-so-far served as mere entertainment to an aspiring futurologist - imagining the world in 30 years where computers can tackle all of the menial
tasks that plague our daily lives. Hark! I do not want to wait 30 years to do nothing!  

So today I have decided to attempt to make my life a little bit easier by attempting something hard. I am going to implement a natural language processing tool that will 
automatically annotate/highlight pdf from input key words and phrases. As a PhD student, I read many many many pdfs on inorganic synthesis, diffraction interpretations, electronic
characterization, etc. Using a tool that can shine through the "word fog" could frankly save me a lot of time, something I find in short supply now-a-days.   

I will be using a github tool guide created by David Mezzetti on [this github page](https://github.com/neuml/txtmarker). 

### Getting Started  

Following the steps outlined by David, I'm first going to install the txtmarker library in a new conda environment using 
> pip install txtmarker

Then, I'll go into my text editor (going with Visual Studio Code) and create a new highlighter
'''python
from txtmarker.factory import Factory
highlighter = Factory.create("pdf")
'''

