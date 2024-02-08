for i in range(num_experiments):
    # Initialize the simulation
    df = init(num_agents, num_patient_zero)
    st = {"Infected": [], "Recovered": [], "Susceptible": []}
    # Simulate one run and collect statistics
    simulate(df, stats=st, nSteps=num_steps)
    all_stats.append(st)