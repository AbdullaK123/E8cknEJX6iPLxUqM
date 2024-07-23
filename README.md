# Potential Talents

## Introduction

In this project, I built a machine learning pipeline to automate canditate selection for a talent sourcing and management company. First I fine-tuned a sentence transformer on our dataset of canditate profiles, and then use them to generate doc embeddings I then used to calculate fitness scores to rank each canditate. Afterwards, I built learning-to-rank models, namely Lambda Rank and Rank Net models, to re-rank canditates should a reviewer choose to star a canditate.

## The Data

Our data is a csv file with the following data dictionary:

Attributes:

id : the unique identifier for each candidate (numeric)

job_title : each canditate's job title (text)

location : the canditate's location (text)

connections: how many connections the canditate has on social media (500+ means over 500 connections) (text)

Output (desired target):

fit - each canditates fitness score (numeric, probability between 0-1)
