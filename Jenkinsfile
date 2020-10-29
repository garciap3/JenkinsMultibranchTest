pipeline {
     agent any
     triggers {
        cron('H */2 * * 1-5')
    }
    // Adds timestamps to the output logged by steps inside the wrapper.
    stages {
        // Just some echoes to show the timestamps.
         stage("First echo"){
              steps {echo "Hey, look, I'm echoing with a timestamp!" }
         }

        // A sleep to make sure we actually get a real difference!
         stage("Sleeping"){
              steps{sleep 30}
         }

        // And a final echo to show the time when we wrap up.
         stage("Second echo"){
              steps{echo "Wonder what time it is now?"}
         }
    }
}
