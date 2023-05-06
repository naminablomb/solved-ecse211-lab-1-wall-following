Download Link: https://assignmentchef.com/product/solved-ecse211-lab-1-wall-following
<br>
<ol>

 <li>Design and implement a <strong>wall</strong>​ following​ system that can navigate around a sequence of blocks and obstacles that form a <strong>wall</strong>​ containing​ gaps, concave corners, and convex corners.</li>

 <li>Implement Bang-Bang and P-type controllers as part of the <strong>wall</strong>​ ​ ​following system.</li>

 <li>Evaluate the design and compare the behavior of the two controllers.</li>

</ol>

<h1>Design requirements</h1>

The following design requirements must be met by your <strong>robot</strong>​ :​

<ul>

 <li><strong>Robot </strong>

  <ul>

   <li>Must be able to complete a lap around a series of blocks while maintaining a fixed distance from the <strong>wall</strong>​ , i.e. a bandcenter.​</li>

   <li>Must account for right-angle convex corners. o Must account for right-angle concave corners. <em>o </em>Must account for gaps in the <strong>wall</strong>​        ​. <em> o            Note: gaps will be no larger than the shortest width of a block, i.e. 10 cm. </em></li>

   <li>Must be able to drive around an arbitrarily shaped <strong>wall</strong>​ , ​ ​<em>made up of at most 7 blocks</em>​.</li>

  </ul></li>

</ul>




<ul>

 <li>Controllers and sensors o Must implement a Bang-Bang controller. o Must implement a P-type controller. o Must use the ultrasonic sensor for range finding. o Must be able to perform the course using each controller type.</li>

</ul>




<h1>DemonstratioN</h1>

The design must satisfy the requirements by completing the demonstration outlined below.

<h2>Design presentation</h2>

Before demoing the design, your group will be asked some questions for less than 5 minutes. You will present your design and answer questions to test your individual understanding of the lab concepts. Each person will be graded individually.

You must also present your workflow, an overview of the hardware design, and an overview of the software functionality. Visualizing software with graphics, such as flow charts, is valuable.

<h2>Bang-bang controller</h2>

<ul>

 <li>Place the <strong>robot</strong>​ ​ at one corner of a sequence​ of blocks as shown in Figure 1.</li>

 <li>Start the <strong>robot</strong>​ ​ with the Bang-Bang controller.​</li>

 <li>The <strong>robot</strong>​ ​ must follow the ​           <strong>wall</strong>​       ​ ​continuously for 2 consecutive laps.</li>

 <li>The <strong>robot</strong>​ ​ cannot touch the ​        <strong>wall</strong>​       ​ at any point,​   including its wires.</li>

</ul>

<h2>P-type controller demo</h2>

<ul>

 <li>Place the <strong>robot</strong>​ ​ at one corner of a sequence​ of blocks as shown in Figure 1.</li>

 <li>Start the <strong>robot</strong>​ ​ with the P-type controller.​</li>

 <li>The <strong>robot</strong>​ ​ must follow the ​           <strong>wall</strong>​       ​ ​continuously for 2 consecutive laps. ● The <strong>robot</strong>​         ​ cannot touch the ​        <strong>wall</strong>​       ​ at any point,​</li>

</ul>

<strong>Figure 1.  Course and robot placement. </strong>

including its wires







<h1>Implementation instructions</h1>

Implement the bangBangController()​ and ​ pTypeController()​            controller methods in the​

UltrasonicController class.​

<strong>      </strong>

<h1>Report Requirements</h1>

The following sections must be included in your report. For this lab, you will not collect any quantitative results; <em>all</em>​<em> data is qualitative</em>​. Answer all questions in the lab report and copy them into your report. For more information, refer to the submission instructions. <strong>Always</strong>​<strong> provide justifications and explanations for all your answers.</strong>

<h2>Section 1: Design Evaluation</h2>

You should concisely explain the overall design of your software and hardware. You must present your workflow, an overview of the hardware design, and an overview of the software functionality. You must briefly talk about your design choices before arriving at your final design. Visualizing hardware and software with graphics (i.e. flowcharts, class diagrams) must be shown. These diagrams are expected to be simple and concise, for example, the class diagram should not include too many low-level details. Make sure to mention how you arrived at tuning your Bang-Bang controller and P-type controller constants (i.e. bandcenter, bandwidth, P-type constant). The design evaluation section is expected to be within <strong>half</strong>​<strong> a page </strong>(​ the graphics would not count towards the limit).

<h2>Section 2: Test Data</h2>

This section describes what data must be collected to evaluate your design requirements. Collect the data using the methodology described below and present it in your report.

<strong>Testing the P-type controller constant </strong>

<ol>

 <li>Choose 2 values above and below your P-type controller constant used in the demo.</li>

 <li>Run the <strong>robot</strong>​ ​ using the ​        <strong>P-type controller</strong>​         .​</li>

 <li>Note its performance, i.e. band center and oscillation behavior, for the 2 cases.</li>

</ol>

<strong>Bang-Bang controller test </strong>(​ <em>3</em>​<em> independent trials</em>​)

<ol>

 <li>Place the <strong>robot</strong>​ ​ at the starting corner of a ​      <strong>wall</strong>​       .​</li>

 <li>Ensure the <strong>wall</strong>​ ​ contains convex corners, concave corners, and gaps.​</li>

 <li>Run the <strong>robot</strong>​ ​ using the ​        <strong>Bang-Bang controller</strong>​              .​</li>

 <li>Check if it completes a lap without touching the <strong>wall</strong>​ .​</li>

 <li>Note its performance, i.e. band center and oscillation behavior for each trial.</li>

</ol>

<strong>P-type controller test </strong>(​ <em>3</em>​<em> independent trials</em>​)

<ol>

 <li>Place the <strong>robot</strong>​ ​ at the starting corner of a ​      <strong>wall</strong>​       .​</li>

 <li>Ensure the <strong>wall</strong>​ ​ contains convex corners, concave corners, and gaps.​</li>

 <li>Run the <strong>robot</strong>​ ​ using the ​        <strong>P-type controller</strong>​         .​</li>

 <li>Check if it completes a lap without touching the <strong>wall</strong>​ .​</li>

 <li>Note its performance, i.e. band center and oscillation behavior for each trial.</li>

</ol>

<h2>Section 3: Test Analysis</h2>

Compare the performance of both controllers. Make sure to refer to your test data.

<ul>

 <li>What happens when your <strong>P-type </strong>​ constant is different from the one used in the demo?​                  How much does your robot oscillate around the band center?</li>

 <li>Did it ever exceed the bandwidth? If so, by how much?</li>

 <li>Describe how this occurs qualitatively for each controller.</li>

</ul>

<h2>Section 4: Observations and Conclusions</h2>

<ul>

 <li>Based on your analysis, which controller would you use and why?</li>

 <li>Does the ultrasonic sensor produce false positives (detection of non-existent objects) and/or false negatives (failure to detect objects)? How frequent were they? Were they filtered?</li>

</ul>

<h2>Section 5: Further Improvements</h2>

<ul>

 <li>What software improvements could you make to address the ultrasonic sensor errors? Give 3 examples.</li>

 <li>What hardware improvements could you make to improve the controller performance? Give 3 examples.</li>

</ul>

What other controller types could be used in place of the <strong>Bang-Bang</strong>​   or​          <strong> P-type</strong>