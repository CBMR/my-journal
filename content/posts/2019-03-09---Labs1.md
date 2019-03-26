---
title: Labs 1
date: "2019-03-09T22:40:32.169Z"
template: "post"
draft: false
slug: "/posts/labs-week-one"
category: "Labs 1"
tags:
  - "Labs"
  - "MongoDB"
  - "GraphQL"

description: "My experience in week one of Labs"
---

**Part One**

Over this sprint, my role was in the backend. For the backend we opted to use Node.js, Express, MongoDB with Mongoose and GraphQL. For the most part, we were using using technologies that we had experience in and we were able to implement it with ease but since we decided to use GraphQL, we had to learn how to use it. Learning how to use it was what took the most amount of time for me. After a couple days of learning it and doing practice queries, I felt comfortable enough to start implementing those queries and mutations. I feel that I successfully accomplished to learn a new tool and implement it into a working backend.

## Detailed Analysis:

One of my tasks was to set up the Customer Type and Mutation. This entitled setting up queries and rootMutations. Queries are how we get data from the database and send it to the front-end. The types of queries that I had to make were setting up ways to get a list of customers and get a customer by ID. rootMutations are a way to either create, update or delete data on the database. I had to create ways to set up a way to create a customer, a way to update a customer. We decided to not allow to delete a record on the database since invoices requires permanent storage of them.

When creating the queries, I had a bit of difficulty because I kept getting an error message that I did not fully understand. It was telling me that the data type “name” was not defined. I took a few minutes to thoroughly read the the error message and also any code that may have had an input on the what was being returned and thanks to that, I was able to find what the issue was. I realized that Mongoose returns data inside of object named “_doc”, so I had to change my code so it returned data from “data._doc” instead. Once I made that change, I was able to fix that issue.

When creating the mutations, I had to research how to set up the updateCustomer mutation. When doing the research, I had to first look up GraphQL docs to see if there were anything different that I had to do, turns out that I did not have to do anything different. So from there, I researched Mongoose and what I had to do there. Mongoose seemed to provide two different ways to update a record in the database. After reviewing both methods, I opted to use the option where I pull in the data, write over the current data that needs updating, and resaving it on the database. I chose this method because it does not override the whole record, just the parts that changed.

**Part Two**

When we were discussing the project as a group on how to set up the project, we all had a lot to offer and input into the conversation. Very early on, we knew we wanted to use technologies that we have not used before, so after discussing as a group, decided to use Java for the backend but we wanted to make sure that it was the best choice. So some of us took a day to review Java and see if it was the best choice. Later on, we all got together and gave our opinions on it. My personal opinion was that Java is a very powerful language but that it was too complex for our needs. It would allow us to perform the operations that we needed but it would also over complicate the backend. I suggested that we stuck with Node.js because it would not only allow us to perform all the necessary operations but that it would also allow us to keep the back-end simple.

Then we had to choose how we were going to query the database, I had really wanted to use GraphQL, so I had been suggesting it from the very beginning and luckily the rest of the team had agreed to use it as well. We all had to research how to use GraphQL for the project. We all learned it different ways. What I did to learn how to use it look over a Udemy course that went over how to use it and also I read multiple technical blogs that discussed GraphQL. From there I was able to start working on the queries.

While working on the back-end, I noticed that we hadn’t fully discussed what kind of data we were going to save on the database and what type of users we will have. So I took it upon myself to create a google document where I went into the tables that we will have in our database and the data types in each of them. I also wrote what types of users there are and the type of access that they have. Once completed, I shared the document with the rest of the team and gave them all editing rights, so they could add anything that may have been missing.
