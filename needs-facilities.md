# Visit-counter for a Facilities Manager

Scenario: Report visitor trends during a week of operation

  Given I store visitor "entry time and date"
  And "out time and date"
  And "type of work" information
  When I perform data analysis on the stored data
  Then I see the visitor trends

Scenario: Alert when seating capacity is full

  Given I have an alert sytem and "seating capacity counter"
  sensor which is working
  When I find "seating capacity counter" equals maximum capacity
  Then I start alert system
