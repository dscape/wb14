
  # Sample Case #1

    * Application crashing in production hundreds
      of times a day
    * High CPU Usage
    * High concurrency level on server (2000/req/s)
    * Huge core dump, small heap dump

    ## Culprit?

      * MongoDB was joining and bringing way too
        much data for each request
      * Unbound joins, e.g. people with a million friends
      * Async.parallel without any `Limit`