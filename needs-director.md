# Visit-counter for a Director

Scenario: Show patient visits during working days and holidays

  Given I have the complete data of patient visits in structured format
  When I retrieve data of patients visited during working days and holidays
  Then I see the results

Scenario: Compute parking slots to reserve for visiting specialists

  Given I have complete data of parking slots
  And visiting specialists
  When I calculate available parking slots
  And number of visiting specialists
  Then I reserve part of parking slots for visiting specialists
