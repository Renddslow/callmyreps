# callmyreps

It has to be easier to call my public officials. This app will send phone scripts via text or notifications about causes people care about. 

This project is in the super duper early stages, so I'm using this to document my thought process with the hopes that other people can help me bring it to life and improve upon it. 

I was really motivated by the SOPA and PIPA campaigns that came out a couple years ago. I took action. I called my representatives because it was super easy. Now, we need to mobilize more than ever. My research shows that phone calls are by far the most effective form of advocacy. What gets in the way is that people don't know what to say. I found this [spreadsheet](https://docs.google.com/spreadsheets/d/174f0WBSVNSdcQ5_S6rWPGB3pNCsruyyM_ZRQ6QUhGmo/htmlview?usp=embed_facebook&sle=true#) that brillantly lays out scripts based on whether someone supports or doesn't support a given issue. 

My thought is that we could use the [Sunlight Foundation API](https://sunlightfoundation.com/api/) that powered the SOPA and PIPA campaigns to help create customized scripts for people. 

I imagine a really simple interface that asks a series of questions: 

1. What's your zipcode? 
2. What issues do you care about? (boolean toggles with fixed categories)
3. How many times per week do you want to call? (default to 3) 
4. When's the best time to get reminders? (boolean toggles for morning, noon, and afternoon) 

The app would send customized scripts based on data pulled from the API. Here are some specific use cases I envision: 

* Citizen follows an issue, such as gun violence prevention. They would recieve notifications, one at a time, with a customized script based on whether their representative's voting record on such an issue. If the representative is pro they would recieve one script, if they are agaisnt, they'd recieve a different script, if there isn't enough information to determine a stance, there would be a different script. The goal is to arm the citizen with as much information as possible so all they have to do is press a button to call. 

* Citizen would be notified with a special script if there is going to be an upcoming vote about a cause they care about. 

##Domain Model

* Citizen (first name, last name, address)[1]
* Script [1]
* Party (Republican, Democrat, Independent, N/A)[2]
* Voting Record (pro, against, neutral)[2]
* Issue (Healthcare, Immigration, Reproductive Rights, etc.)[1] 
* Representative [2]
  * National Representative (Senator, House)
  * State Representative (Governor, State Senate, State House)
  * Local Representative (School Board, Special Districts, Board of Supervisor, Town/City Council, Mayor, etc.) 
* District (geographic region within which people vote for a certain office) [2]
* Time to Call (morning, noon, afternoon, evening)[1]
* Calling Frequency (# of times per week)[1]

[1] - written in app, refererenced from [calling sheet](https://docs.google.com/spreadsheets/d/174f0WBSVNSdcQ5_S6rWPGB3pNCsruyyM_ZRQ6QUhGmo/htmlview?usp=embed_facebook&sle=true#)   
[2] - From [Sunlight Foundation](https://sunlightfoundation.com/api/) or other API

##How to Contribute

1. Create or sign into your GitHub account

2. Click on the issues button at the top of the page. 

3. Filter issues based on labels. There's work for visual designers, UX/UI, copywriters, and people who are domain experts but don't write code. You do not have to know how to code to contribute. Post a comment and submit work. 
