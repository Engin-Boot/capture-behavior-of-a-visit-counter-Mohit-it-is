# Visit-counter technical needs

Scenario: Recover across restarts of the server
that runs the visit-counter

  Given I have local "visit-counter" storage system linked
  with server "visit-counter"
  When I find local "visit-counter" is not equal to
  server "visit-counter"
  Then I perfrom synchronization

Scenario: Reconcile counts if the sensor is offline for a while

  Given I have backup sensor and primary sensor for "visit-counter"
  When primary sensor goes offline
  Then Run backup sensor 
