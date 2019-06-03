# DRL_Collaboration-and-Competition


<div class="_main--content-container--ILkoI"><div><div class="index--container--2OwOl"><div class="index--atom--lmAIo layout--content--3Smmq"><div class="ltr"><div class="index-module--markdown--2MdcR ureact-markdown "><h1 id="the-environment">The Environment</h1>
</div></div><span></span></div></div></div><div><div class="index--container--2OwOl"><div class="index--atom--lmAIo layout--content--3Smmq"><div class="ltr"><div class="index-module--markdown--2MdcR ureact-markdown "><p>For this project, I worked with the <a target="_blank" href="https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#tennis">Tennis</a> environment.  </p>
  
</div></div><span></span></div></div></div><div><div class="index--container--2OwOl"><div class="index--atom--lmAIo layout--content--3Smmq"><div><a href="#" class="image-atom--image-atom--1XDdu"><div class="index--image-atom-content--YoZVu"><div class="index--image-and-annotations-container--1o6QP"><img src="https://s3.amazonaws.com/video.udacity-data.com/topher/2018/May/5af7955a_tennis/tennis.png" alt="Unity ML-Agents Tennis Environment" width="600px" class="index--image--1wh9w"></div><div class="index--caption--34paT"><div class="index-module--markdown--2MdcR ureact-markdown "><p>Unity ML-Agents Tennis Environment</p>
</div></div></div></a></div><span></span></div></div></div><div><div class="index--container--2OwOl"><div class="index--atom--lmAIo layout--content--3Smmq"><div class="ltr"><div class="index-module--markdown--2MdcR ureact-markdown "><p>In this environment, two agents control rackets to bounce a ball over a net. If an agent hits the ball over the net, it receives a reward of +0.1.  If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01.  Thus, the goal of each agent is to keep the ball in play.</p>
<p>The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation.  Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping. </p>
<p>The task is episodic, and in order to solve the environment, the agents must get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents). Specifically,</p>
<ul>
<li>After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 2 (potentially different) scores. We then take the maximum of these 2 scores.</li>
<li>This yields a single <strong>score</strong> for each episode.</li>
</ul>
<p>The environment is considered solved, when the average (over 100 episodes) of those <strong>scores</strong> is at least +0.5.</p>
<h2 id="note">Note</h2>
<hr>
<p>The project environment is similar to, but <strong>not identical to</strong> the Tennis environment on the <a target="_blank" href="https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md">Unity ML-Agents GitHub page</a>.  </p>
</div></div><span></span></div></div></div></div>


<div class="_main--content-container--ILkoI"><div><div class="index--container--2OwOl"><div class="index--atom--lmAIo layout--content--3Smmq"><div class="ltr"><div class="index-module--markdown--2MdcR ureact-markdown "><h1 id="the-environment">Installation </h1>
</div></div><span></span></div></div></div><div><div class="index--container--2OwOl"><div class="index--atom--lmAIo layout--content--3Smmq"><div class="ltr"><div class="index-module--markdown--2MdcR ureact-markdown "><p>Follow the instructions below to explore the environment on your own machine!  You will also learn how to use the Python API to control your agent.</p>
<h2 id="step-1-activate-the-environment">Step 1: Activate the Environment</h2>
<hr>
<p>If you haven't already, please follow the <a target="_blank" href="https://github.com/udacity/deep-reinforcement-learning#dependencies">instructions in the DRLND GitHub repository</a> to set up your Python environment.  These instructions can be found in <code>README.md</code> at the root of the repository.  By following these instructions, you will install PyTorch, the ML-Agents toolkit, and a few more Python packages required to complete the project.</p>
<p>(<em>For Windows users</em>) The ML-Agents toolkit supports Windows 10. While it might be possible to run the ML-Agents toolkit using other versions of Windows, it has not been tested on other versions. Furthermore, the ML-Agents toolkit has not been tested on a Windows VM such as Bootcamp or Parallels.  </p>
<blockquote>
<p><strong>SPECIAL NOTE TO BETA TESTERS</strong> - please also download the <code>p3_collab-compet</code> folder from <a target="_blank" href="https://s3-us-west-1.amazonaws.com/udacity-drlnd/tmp/p3_collab-compet.zip">here</a> and place it in the DRLND GitHub repository.</p>
</blockquote>
<h2 id="step-2-download-the-unity-environment">Step 2: Download the Unity Environment</h2>
<hr>
<p>For this project, you will <strong>not</strong> need to install Unity - this is because we have already built the environment for you, and you can download it from one of the links below.  You need only select the environment that matches your operating system:</p>
<ul>
<li>Linux: <a target="_blank" href="https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip">click here</a></li>
<li>Mac OSX: <a target="_blank" href="https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis.app.zip">click here</a></li>
<li>Windows (32-bit): <a target="_blank" href="https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86.zip">click here</a></li>
<li>Windows (64-bit): <a target="_blank" href="https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip">click here</a></li>
</ul>
<p>Then, place the file in the <code>p3_collab-compet/</code> folder in the DRLND GitHub repository, and unzip (or decompress) the file.</p>
<p>(<em>For Windows users</em>) Check out <a target="_blank" href="https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64">this link</a> if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.</p>
<p>(<em>For AWS</em>) If you'd like to train the agent on AWS (and have not <a target="_blank" href="https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md">enabled a virtual screen</a>), then please use <a target="_blank" href="https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux_NoVis.zip">this link</a> to obtain the "headless" version of the environment.  You will <strong>not</strong> be able to watch the agent without enabling a virtual screen, but you will be able to train the agent.  (<em>To watch the agent, you should follow the instructions to <a target="_blank" href="https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md">enable a virtual screen</a>, and then download the environment for the <strong>Linux</strong> operating system above.</em>)</p>
<hr>
 </p>
  
 <p>Finally, use the <code>Requirement.txt</code> file to install all the library that the project needed.  </p>
  
</div></div><span></span></div></div></div></div>


##Report

<p>After you have followed the instructions above, open <code>Tennis.ipynb</code> (located in the <code>p3_collab-compet/</code> folder in the DRLND GitHub repository) and follow the instructions to learn how to use the Python API to control the agent.</p>
<p>Watch the (<em>silent</em>) video below to see what kind of output to expect from the notebook, if everything is working properly! 
