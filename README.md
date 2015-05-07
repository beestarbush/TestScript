# TestScript

echo "## AudioMuteScript ##"
echo "What process you want to get? (DEFAULT:AudioBla) : "
read processName
processID="$(ps | grep $processName | awk '{ print $1 }')"
echo "Process ID of process: $processID" 

echo "Please enter a scenario: "
read userChosenScenario
echo "Chosen scenario is: $userChosenScenario"

case $userChosenScenario in
        "A")
                if [ $processName = "bash" ]
                then
                        echo "Process is bash with PID: $processID"
                fi
                ;;
        "B")
                echo "Say B"
                ;;
        *)
                echo "Non valid choice"
                ;;
esac

