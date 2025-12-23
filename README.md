# langchain-ai
The industry standard for building LLM apps
#Define a researcher agent
researcher=agent(
 role='senior researcher',
 goal='Uncover latest trends in AI 2025',
 backstory="you are an expert at identifying emerging technologies.",
 verbose=true
 )

Define a writer agent
writer=agent
 role='tech content strategist',
 gole='Write a blog post based on research',
 backstory="You simplify complex tech into engaging articles.",
 verbose=True
 )

#Create task and execute
task1=Task(description='Analyze AI trends 2025',
agent=researcher)
task2=Task(description='Write a 500- word summary',
agent=writer)

crew=Crew(agents=[researcher,writer],tasks=[task1,task2])
result=crew.kickoff()
print(result)
