Dear Dr. Aliakbarpour,

I apologize for the delay - spring break was fairly disruptive. I recently finished reading your paper, _"High-Probability Bounds for Heterogeneous Local Differential Privacy,"_ which you recommended.

I found the results very compelling, particularly the derivation of tight high-probability bounds for heterogeneous LDP (beyond in-expectation guarantees) and the improvement from multiplicative to additive penalties in the multi-dimensional setting.

I had a few questions:

- The heterogeneous privacy budgets are modeled as a vector $\vec{\epsilon}$, where each user $i$ has a scalar $\epsilon_i$ applied across their entire data point. Could this be extended to a user-by-attribute matrix for multi-dimensional data, allowing attribute-level privacy (e.g., stronger privacy for location than age)? If so, how might this affect the additive error bounds?
- The method weights users according to their privacy levels, placing more emphasis on those with larger $\epsilon_i$. Could introducing a separate notion of “confidence” or “trustworthiness” in user data meaningfully refine the error bounds? For instance, what happens if a user reports an unusually large $\epsilon_i$ that disproportionately influences the estimate?

I also read your paper, _"Optimal Algorithms for Augmented Testing of Discrete Distributions."_ I found the framework of incorporating a prediction - while preserving optimal asymptotic guarantees and relaxing assumptions via total variation distance - particularly elegant.

One possible extension I was curious about:

- The current framework considers a single predicted model. Could this be generalized to handle multiple predictions (e.g., from different models or data sources), perhaps via adaptive weighting based on accuracy or pruning? This seems like a natural direction in practical settings - has this been explored?

Thank you again for sharing these papers. I would greatly appreciate the opportunity to discuss these ideas further.

Best regards,  
Anthony Schurle
