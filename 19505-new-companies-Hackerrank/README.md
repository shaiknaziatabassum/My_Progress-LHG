# [New Companies](https://www.hackerrank.com/challenges/the-company/problem?isFullScreen=true)
## Medium
<div class="challenge-body-html"><div class="challenge_problem_statement"><div class="msB challenge_problem_statement_body"><div class="hackdown-content"><svg style="display: none;"><defs id="MathJax_SVG_glyphs"></defs></svg><p>Amber's conglomerate corporation just acquired some new companies. Each of the companies follows this hierarchy: <img src="https://s3.amazonaws.com/hr-challenge-images/19505/1458531031-249df3ae87-ScreenShot2016-03-21at8.59.56AM.png"></p>

<p>Given the table schemas below, write a query to print the <em>company_code</em>, <em>founder</em> name, total number of <em>lead</em> managers, total number of <em>senior</em> managers, total number of <em>managers</em>, and total number of <em>employees</em>. Order your output by ascending <em>company_code</em>.</p>

<p><strong>Note:</strong></p>

<ul>
<li>The tables may contain duplicate records.</li>
<li>The <em>company_code</em> is string, so the sorting should not be <strong>numeric</strong>. For example, if the <em>company_codes</em> are <em>C_1</em>, <em>C_2</em>, and <em>C_10</em>, then the ascending <em>company_codes</em> will be <em>C_1</em>, <em>C_10</em>, and <em>C_2</em>.</li>
</ul>

<hr></div></div></div><div class="challenge_input_format"><div class="msB challenge_input_format_title"><p><strong>Input Format</strong></p></div><div class="msB challenge_input_format_body"><div class="hackdown-content"><svg style="display: none;"><defs id="MathJax_SVG_glyphs"></defs></svg><p>The following tables contain company data:</p>

<ul>
<li><p><em>Company:</em> The <em>company_code</em> is the code of the company and <em>founder</em> is the founder of the company. <img src="https://s3.amazonaws.com/hr-challenge-images/19505/1458531125-deb0a57ae1-ScreenShot2016-03-21at8.50.04AM.png"></p></li>
<li><p><em>Lead_Manager:</em> The <em>lead_manager_code</em> is the code of the lead manager, and the <em>company_code</em> is the code of the working company. <img src="https://s3.amazonaws.com/hr-challenge-images/19505/1458534960-2c6d764e3c-ScreenShot2016-03-21at8.50.12AM.png"></p></li>
<li><p><em>Senior_Manager:</em> The <em>senior_manager_code</em> is the code of the senior manager, the <em>lead_manager_code</em> is the code of its lead manager, and the <em>company_code</em> is the code of the working company. <img src="https://s3.amazonaws.com/hr-challenge-images/19505/1458534973-6548194998-ScreenShot2016-03-21at8.50.21AM.png"></p></li>
<li><p><em>Manager:</em> The <em>manager_code</em> is the code of the manager, the <em>senior_manager_code</em> is the code of its senior manager, the <em>lead_manager_code</em> is the code of its lead manager, and the <em>company_code</em> is the code of the working company. <img src="https://s3.amazonaws.com/hr-challenge-images/19505/1458534988-7fc0af46ce-ScreenShot2016-03-21at8.50.29AM.png"></p></li>
<li><p><em>Employee:</em> The <em>employee_code</em> is the code of the employee, the <em>manager_code</em> is the code of its manager, the <em>senior_manager_code</em> is the code of its senior manager, the <em>lead_manager_code</em> is the code of its lead manager, and the <em>company_code</em> is the code of the working company. <img src="https://s3.amazonaws.com/hr-challenge-images/19505/1458535002-d47f63cbb4-ScreenShot2016-03-21at8.50.41AM.png"></p></li>
</ul>

<hr></div></div></div><div class="challenge_sample_input"><div class="msB challenge_sample_input_title"><p><strong>Sample Input</strong></p></div><div class="msB challenge_sample_input_body"><div class="hackdown-content"><svg style="display: none;"><defs id="MathJax_SVG_glyphs"></defs></svg><p><em>Company</em> Table: <img src="https://s3.amazonaws.com/hr-challenge-images/19505/1458535049-2a207c44b3-ScreenShot2016-03-21at8.50.52AM.png">
<em>Lead_Manager</em> Table: <img src="https://s3.amazonaws.com/hr-challenge-images/19505/1458535073-919107f639-ScreenShot2016-03-21at8.51.03AM.png">
<em>Senior_Manager</em> Table: <img src="https://s3.amazonaws.com/hr-challenge-images/19505/1458535111-b1c48335b3-ScreenShot2016-03-21at8.51.15AM.png">
<em>Manager</em> Table: <img src="https://s3.amazonaws.com/hr-challenge-images/19505/1458535122-888f4bf340-ScreenShot2016-03-21at8.51.26AM.png">
<em>Employee</em> Table: <img src="https://s3.amazonaws.com/hr-challenge-images/19505/1458535134-878767e0d9-ScreenShot2016-03-21at8.51.52AM.png"></p></div></div></div><div class="challenge_sample_output"><div class="msB challenge_sample_output_title"><p><strong>Sample Output</strong></p></div><div class="msB challenge_sample_output_body"><div class="hackdown-content"><svg style="display: none;"><defs id="MathJax_SVG_glyphs"></defs></svg><pre><code>C1 Monika 1 2 1 2
C2 Samantha 1 1 2 2
</code></pre></div></div></div><div class="challenge_explanation"><div class="msB challenge_explanation_title"><p><strong>Explanation</strong></p></div><div class="msB challenge_explanation_body"><div class="hackdown-content"><svg style="display: none;"><defs id="MathJax_SVG_glyphs"></defs></svg><p>In company <em>C1</em>, the only lead manager is <em>LM1</em>. There are two senior managers, <em>SM1</em> and <em>SM2</em>, under <em>LM1</em>. There is one manager, <em>M1</em>, under senior manager <em>SM1</em>. There are two employees, <em>E1</em> and <em>E2</em>, under manager <em>M1</em>.</p>

<p>In company <em>C2</em>, the only lead manager is <em>LM2</em>. There is one senior manager, <em>SM3</em>, under <em>LM2</em>. There are two managers, <em>M2</em> and <em>M3</em>, under senior manager <em>SM3</em>. There is one employee, <em>E3</em>, under manager <em>M2</em>, and another employee, <em>E4</em>, under manager, <em>M3</em>.</p></div></div></div></div>