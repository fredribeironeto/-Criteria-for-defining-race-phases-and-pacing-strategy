# -Criteria-for-defining-race-phases-and-pacing-strategy
A method using an open-source Python routine for establishing criteria for the phases of the 200-meter kayak and canoe paralympic canoe sprint race based on pacing strategies through the application of a mathematical approach of a piecewise linear least fit. 

The following steps serve as a guide to demonstrate one way of utilizing the current Python routine employed in the present study. Anaconda software (version 2.5.4, Anaconda Software Distribution, Austin, TX) was utilized, providing a pre-configured Python development environment for data analysis. The script is implemented in Jupyter Notebook (version 3.3.2, Project JupyterLab, US),1 leveraging Python and additional code snippets. Alternative options are available, and the Python routine is an open-source distribution, allowing users to make enhancements.
1.	Install Anaconda software (https://www.anaconda.com/download), which provides access to the Jupyter Notebook environment to run Python files.
2.	Using Anaconda’s terminal (CMD.exe Prompt), install the Python library known as "pwlf" (piecewise linear fitting), using the command: conda install -c conda-forge pwlf (https://jekel.me/piecewise_linear_fit_py/installation.html#conda).
3.	Create an Excel file (.xlsx) with a single sheet and three columns in the following order and named as “Seconds”, “Odometer”, and “Velocity.” The file must be in the same folder as the Python routines (AnaliseGPSkayakV5.ipynb for kayak or AnaliseGPSCanoeV5.ipynb for canoe).
4.	To include a new athlete to be analyzed in the Python routine, the Python file must be opened in Jupyter notebook. Inside the fifth box, the Excel file name must be added to the Python routine:
4.1 Add the file name:
	dados1 = pd.read_excel(“AAAAAA.xlsx”)
	dados2 = pd.read_excel(“BBBBBB.xlsx”)
	dados(n) = pd.read_excel(“CCCCCC.xlsx”)
4.2 Add the file name to the list:
	listaDados = [dados1, dados2, dados(n)]
4.3 Provide file identification:
	listaID = [‘Athlete 1’, ‘Athlete2’, ‘Athlete(n)’]
5.	Finally, you can adjust the desired number of phases or specify a percentage improvement in the model with an additional phase (i.e., reduction in the quadratic error):
limitepercent = n
maxCurvas = n
Where "limitepercent" represents the percentage improvement, "maxCurvas" indicates the number of phases, and "n" is the desired value.
 
REFERENCES

1. 	Perez F, Granger BE. IPython: A System for Interactive Scientific Computing. Comput Sci Eng 2007; 9: 21–29.
