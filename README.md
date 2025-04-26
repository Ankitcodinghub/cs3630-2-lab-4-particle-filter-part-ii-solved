# cs3630-2-lab-4-particle-filter-part-ii-solved
**TO GET THIS SOLUTION VISIT:** [CS3630-2 Lab 4-PARTICLE FILTER PART II Solved](https://www.ankitcodinghub.com/product/cs3630-2-cs-3630-introduction-to-robotics-and-perception-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;111218&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS3630-2 Lab 4-PARTICLE FILTER PART II  Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
LAB 4: PARTICLE FILTER PART II

The 4th Annual CS 3630 Skating Competition

enable Skater-Bot to skate within its arena and reach a target marker. In order to reach this goal,

you must implement three functions: marker_processing(), compute_odometry(), and run().Each function implementation detail can be found in the section below.

Important note: Unlike previous labs, in this assignment we will treat all symbols as interchangeable. In other words, all the robot needs to know is that it saw a ‘marker/symbol’, but not which one. Do not hard code the locations of the symbols into your code since we will randomize their location during grading.

Localization: The main component of the lab is to use your particle filter from Lab 3 to enable the robot to 1) determine where it is, and 2) use this information to go to a predefined goal location on the map. We have provided a starter file, called go_to_goal.py, which contains the following functions:

The main processing loop should:

• Obtain odometry information

• Update the particle filter using the above information

• Update the particle filter GUI (for debugging)

• Have the robot drive to the goal, which is given as (6², 10², 0). Note that the goal is defined in terms of both position (x,y) = (6 inches, 10 inches) and orientation h = 0 degrees. Once there, have the robot play a happy animation and then stand still.

• Make your code robust to the “kidnapped robot problem” by resetting your localization if the robot is picked up. This should trigger both when the robot is on its way to the goal and once it has reached it (i.e. picking up the robot from the goal and placing it somewhere else should immediately cause it to try to localize itself and search for the goal again).

You are encouraged to reuse as much of your existing code as possible for this lab. The coordinate frame we are using is:

Note: this picture is just used for explaining coordinate frames. Please setup marker positions as in ‘Setup’ section.

Grading: The assignment will be assessed based on the Code portion and the Video portion. The

Code portion will be evaluated on passing all the visible and hidden test cases in Gradescope. The Video portion will be evaluated for 1) obtaining the correct robot position and orientation estimate, 2) enabling the robot to successfully drive to the goal. The Code will count as 30% of your grade, and the Video portion will count as 70% of your grade.

Note and Suggestions:

1. Do not create problematic situations, such as starting the robot facing a corner.

Our grading rubric for the Video portion will look like this:

Run PF correctly converged Reached goal Reset on kidnap Total

1 /35 /25 /10 /70

Grading notes:

• PF correctly converged: Full credit if the PF estimate at any point matches the real robot pose. Position should be within 3” and angle should be within 15 degrees of real robot pose. It’s fine if the PF does not stay converged, full credit will be awarded if it converges to the right pose at any time. Within the video, you need to show the moment that PF correctly converged on your computer screen as the robot is moving within the arena.

• Reached goal: Full credit if the robot center is within 3” of the goal. 5 points if the angle of the robot is within 15 degrees of the specified angle.

• Reset on kidnap: Full credit if the PF resets to a uniform distribution if the robot is picked up. Within the video, you need to show your computer screen that PF distribution is uniform as you pick up the robot after it reaches a marker.

Submission: Submit your go_to_goal_cozmo/vector.py file and video file, make sure you enter the names of both partners in a comment at the top of the file. Make sure the file remains compatible with the autograder. Only one partner should upload the file to Gradescope. If you relied significantly on any external resources to complete the lab, please reference these in the submission comments.
