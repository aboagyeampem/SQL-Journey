-- Questions
-- Provide a table for all web_events associated with account name of Walmart. 
-- There should be three columns. Be sure to include the primary_poc, time of the event, 
-- and the channel for each event. Additionally, you might choose to add a fourth column to 
-- assure only Walmart events were chosen.


-- Answer
SELECT a.primary_poc, 
	w.occurred_at, 
       	w.channel,
	a.name
FROM accounts a
JOIN web_events w
ON a.id = w.account_id
WHERE a.name = 'Walmart' 

-- Results named only_walmart.csv
