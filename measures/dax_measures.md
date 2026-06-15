# DAX Measures
average_score2026 = 
CALCULATE(
    AVERAGE(vaibhav_sooryavanshi_ipl_data[score]),
    vaibhav_sooryavanshi_ipl_data[year]= 2026
)

average_score25 = 
CALCULATE(
    AVERAGE(vaibhav_sooryavanshi_ipl_data[score]),
    vaibhav_sooryavanshi_ipl_data[year]= 2025
)

AVG_score = AVERAGE(vaibhav_sooryavanshi_ipl_data[score])

batting_average = DIVIDE([total_runs],[total_outs])

boundary_percentage = DIVIDE([boundary_runs],[total_runs])*100
boundary_runs = SUM(vaibhav_sooryavanshi_ipl_data[4s])+SUM(vaibhav_sooryavanshi_ipl_data[6s])
consistencyscore = AVERAGE(vaibhav_sooryavanshi_ipl_data[score])/STDEV.P(vaibhav_sooryavanshi_ipl_data[score])
dotball% = DIVIDE(SUM(vaibhav_sooryavanshi_ipl_data[dot_balls]),[total_balls])*100
fiftees = CALCULATE(COUNTROWS(vaibhav_sooryavanshi_ipl_data),vaibhav_sooryavanshi_ipl_data[score]>49,vaibhav_sooryavanshi_ipl_data[score]<100)
highest_score = MAX(vaibhav_sooryavanshi_ipl_data[score])
hundred = CALCULATE(COUNTROWS(vaibhav_sooryavanshi_ipl_data),vaibhav_sooryavanshi_ipl_data[score]>99)
lowest_score = min(vaibhav_sooryavanshi_ipl_data[score])
Runs Growth % = 
DIVIDE(
    [total_runs] - [runs2025],
    [runs2025]
) * 100

runs2025 = CALCULATE(SUM(vaibhav_sooryavanshi_ipl_data[score]),vaibhav_sooryavanshi_ipl_data[year]=2025)

str_rate = divide([total_runs],[total_balls])*100
total_balls = Sum(vaibhav_sooryavanshi_ipl_data[balls_taken])
total_fours = sum(vaibhav_sooryavanshi_ipl_data[4s])
total_outs = COUNT(vaibhav_sooryavanshi_ipl_data[dismissal])
total_runs = Sum(vaibhav_sooryavanshi_ipl_data[score])
total_six = Sum(vaibhav_sooryavanshi_ipl_data[6s])
yoy_growth_average = [average_score2026]-[average_score25]



