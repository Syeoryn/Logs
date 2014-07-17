#### July 16, 2014
  * All My Teachers are Holograms:
    * Looping seek events
      Symptoms:
      <ul>
       Seeking without pausing (particularly rewinding) causes video to skip back and forth between new time and old time for all users in hangout
      </ul>
      Issue:
      <ul>
        Believed that the lag in event transmission and internet speed caused the time to be updated in the responders hangout to the correct time, but a time that was prior to the initializers time (since the video continued playing).  This caused the seek event to be triggered multiple times for each participant in the hangout.
      </ul>
      Solution:
      <ul>
        Used [1 second] throttle function to prevent seek from being called/ triggered in response to itself
      </ul>