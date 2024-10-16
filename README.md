<!DOCTYPE html>
<html>
<head>
    <title>Minimizing Energy Consumption in Computer Networks via Convex Optimization</title>
</head>
<body>

<h1>Minimizing Energy Consumption in Computer Networks via Convex Optimization</h1>

<p>This repository contains the code and documentation for the project titled <strong>"Minimizing Energy Consumption in Computer Networks via Convex Optimization"</strong> by <strong>Mohammad Raihan Uddin</strong>.</p>

<h2>Table of Contents</h2>

<ul>
    <li><a href="#introduction">Introduction</a></li>
    <li><a href="#system-model-and-problem-formulation">System Model and Problem Formulation</a></li>
    <li><a href="#requirements">Requirements</a></li>
    <li><a href="#installation">Installation</a></li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#simulation-results">Simulation Results</a></li>
    <li><a href="#project-structure">Project Structure</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact-information">Contact Information</a></li>
</ul>

<hr>

<h2 id="introduction">Introduction</h2>

<p>Energy efficiency is a critical aspect of modern computer networks. This project presents a convex optimization approach to minimize energy consumption by jointly optimizing CPU frequency and transmit power under various constraints. Frequency Division Multiple Access (FDMA) is employed as the transmission protocol. The objective is to explore trade-offs between energy consumption, system performance, and operational constraints through simulation scenarios.</p>

<hr>

<h2 id="system-model-and-problem-formulation">System Model and Problem Formulation</h2>

<p>The network consists of multiple user devices (UDs) that execute tasks locally and offload data to a base station (BS) for further processing. The optimization problem aims to minimize the total energy consumption of all UDs by adjusting the CPU frequencies and transmit powers while satisfying constraints such as latency, power limits, and processing capabilities.</p>

<p>The problem is formulated as a convex optimization problem, utilizing techniques like Successive Convex Approximation (SCA) to handle non-convexities in the objective function and constraints.</p>

<p>For detailed mathematical formulations and derivations, please refer to the <a href="paper.pdf">project paper</a> included in this repository.</p>

<hr>

<h2 id="requirements">Requirements</h2>

<ul>
    <li><strong>MATLAB</strong> (R2018b or later recommended)</li>
    <li><strong>YALMIP</strong> toolbox (<a href="https://yalmip.github.io/download/">Download YALMIP</a>)</li>
    <li><strong>Optimization Solvers</strong> compatible with YALMIP (e.g., <code>fmincon</code>, <code>SDPT3</code>, <code>SeDuMi</code>)</li>
    <li><strong>LaTeX</strong> distribution (e.g., TeX Live, MiKTeX) for compiling the paper (optional)</li>
    <li><strong>Git</strong> (for cloning the repository)</li>
</ul>

<hr>

<h2 id="installation">Installation</h2>

<h3>Clone the Repository</h3>

<pre><code>git clone https://github.com/yourusername/minimizing-energy-consumption.git
</code></pre>

<h3>Set Up MATLAB Environment</h3>

<ol>
    <li><strong>Add YALMIP to MATLAB Path</strong>

    <p>Open MATLAB and add the YALMIP toolbox to your MATLAB path:</p>

    <pre><code>addpath(genpath('path_to_yalmip_folder'));
savepath;
</code></pre>

    <p>Replace <code>'path_to_yalmip_folder'</code> with the actual path where YALMIP is installed.</p>
    </li>

    <li><strong>Ensure Solver Compatibility</strong>

    <p>Make sure you have an appropriate solver installed. You can check available solvers using:</p>

    <pre><code>yalmip('allsolvers');
</code></pre>
    </li>
</ol>

<h3>Set Up LaTeX Environment (Optional)</h3>

<p>If you wish to compile the LaTeX document (<code>paper.tex</code>), ensure you have a LaTeX distribution installed.</p>

<hr>

<h2 id="usage">Usage</h2>

<h3>Running the Optimization Script</h3>

<ol>
    <li><strong>Navigate to Project Directory</strong>

    <p>Open MATLAB and change the current folder to the project directory:</p>

    <pre><code>cd 'path_to_project_directory';
</code></pre>
    </li>

    <li><strong>Run the Main Script</strong>

    <p>Execute the optimization script:</p>

    <pre><code>run('energy_optimization.m');
</code></pre>

    <p><em>(Replace <code>energy_optimization.m</code> with the actual script name.)</em></p>
    </li>

    <li><strong>View Results</strong>

    <p>The script will perform the optimization, display results in the command window, and generate plots illustrating the optimization process.</p>
    </li>
</ol>

<h3>Compiling the LaTeX Document</h3>

<ol>
    <li><strong>Navigate to Project Directory</strong>

    <p>In your terminal or command prompt, navigate to the project directory.</p>
    </li>

    <li><strong>Compile the Document</strong>

    <p>Compile the <code>paper.tex</code> file using a LaTeX compiler:</p>

    <pre><code>pdflatex paper.tex
</code></pre>

    <p>Repeat the compilation if necessary to resolve references.</p>
    </li>

    <li><strong>View the PDF</strong>

    <p>Open <code>paper.pdf</code> to read the detailed project report.</p>
    </li>
</ol>

<hr>

<h2 id="simulation-results">Simulation Results</h2>

<p>The simulation results demonstrate the effectiveness of the convex optimization approach in reducing energy consumption. Key findings include:</p>

<ul>
    <li><strong>Optimal CPU Frequency:</strong> \( f_u = 1.20 \times 10^9 \, \text{Hz} \)</li>
    <li><strong>Optimal Transmit Power:</strong> \( p_u = 0.002000 \, \text{W} \)</li>
    <li><strong>Optimal Slack Variable:</strong> \( x_u = 6.406443 \, \text{s} \)</li>
    <li><strong>Total Latency:</strong> \( 6.823108 \, \text{s} \)</li>
    <li><strong>Total Energy Consumption:</strong> \( 0.084814 \, \text{J} \)</li>
</ul>

<p><strong>Generated Plots:</strong></p>

<ul>
    <li><strong>Figure 1:</strong> Energy consumption vs. Iterations</li>
    <li><strong>Figure 2:</strong> Transmit power vs. Iterations</li>
    <li><strong>Figure 3:</strong> Total energy consumption vs. Slack variable</li>
</ul>

<p>These results indicate that jointly optimizing CPU frequency and transmit power significantly reduces energy consumption while satisfying latency constraints.</p>

<hr>

<h2 id="project-structure">Project Structure</h2>

<ul>
    <li><code>energy_optimization.m</code>: MATLAB script implementing the optimization algorithm.</li>
    <li><code>paper.tex</code>: LaTeX source code for the project report.</li>
    <li><code>paper.pdf</code>: Compiled PDF of the project report.</li>
    <li><code>figures/</code>: Directory containing figures used in the report.</li>
    <li><code>README.md</code>: This README file.</li>
    <li><code>.gitignore</code>: Git ignore file specifying files to exclude from version control.</li>
</ul>

<hr>

<h2 id="contributing">Contributing</h2>

<p>Contributions to this project are welcome. If you have suggestions for improvements or encounter any issues, please open an issue or submit a pull request.</p>

<p><strong>To contribute:</strong></p>

<ol>
    <li>Fork the repository.</li>
    <li>Create a new branch:

    <pre><code>git checkout -b feature/your-feature-name
</code></pre>
    </li>

    <li>Commit your changes:

    <pre><code>git commit -am 'Add your feature'
</code></pre>
    </li>

    <li>Push to the branch:

    <pre><code>git push origin feature/your-feature-name
</code></pre>
    </li>

    <li>Open a pull request.</li>
</ol>

<hr>

<h2 id="license">License</h2>

<p>This project is licensed under the <strong>MIT License</strong>. See the <a href="LICENSE">LICENSE</a> file for details.</p>

<hr>

<h2 id="contact-information">Contact Information</h2>

<ul>
    <li><strong>Author:</strong> Mohammad Raihan Uddin</li>
    <li><strong>Email:</strong> <a href="mailto:your.email@example.com">your.email@example.com</a></li>
</ul>

<hr>

<p><em>Please replace <code>yourusername</code>, <code>your.email@example.com</code>, and file paths with your actual information.</em></p>

<hr>

<h3>Additional Notes</h3>

<ul>
    <li><strong>Documentation:</strong> The MATLAB code is well-commented for clarity.</li>
    <li><strong>Issues:</strong> If you encounter any problems, please report them in the Issues section of the repository.</li>
    <li><strong>Updates:</strong> Regular updates and improvements will be made to enhance the project's functionality.</li>
</ul>

<hr>

</body>
</html>
