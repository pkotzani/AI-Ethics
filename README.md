# AI-Ethics
Empirical evaluation of 8 LLMs using 5 domain-specific ethical dilemmas, to assess their behavior under different ethical principle prioritizations. By modifying the prioritization of ethical principles, we assess the effects on the decision outcomes, consistency and convergence of responses, within and across models and user runs. 

# Scope
We experimentally examine the effect of ethical prioritization in LLM behavior. We use ethical dilemmas spanning different sectors and context, to initially examine the behavior of LLMs based on their initial ethical training. Then without modifying their underlying ethical principles, we modify the prioritization among those principles to examine how this affects the consistency and convergence of responses within and across LLMs. 

## Selection and definition of ethical dilemmas 
Ethical dilemmas refer to situations where deciding what is right or wrong is non-obvious or even controversial. In addition, the morality of the decision may vary depending on the applied ethical framework; a decision considered ethically moral under deontological ethics, may be immoral under utilitarianism or virtue ethics. 
One of the most famous examples of ethical dilemmas is "the trolley problem". In its simplest form, a runaway trolley is headed towards five people, and the only way to save them is to press a button that will switch the trolley to a different track, eventually killing one person instead of five. Under consequentialism,  pressing the button is the most ethical decision, since it will benefit the most (maximizing beneficence) and harm less people (minimizing maleficence). However, under deontology, pressing the button is unethical, since it _actively_ violates the principle of treating all individuals as ends in themselves, with dignity and rights (fairness and justice are equal for all).

Besides their role in promoting critical thinking and revealing the complexities of ethics, arguments against such dilemmas emphasize inherent inconsistencies and the possibility of alternatives in realistic and less synthetic situations. Although this debate is beyond the scope of this work, for our purpose we have synthesized and applied 5 different dilemmas, based on the following criteria:

1) Describe scenarios _applicable in autonomous AI applications_, i.e., cases where AI components may take a decision even without human intervention.
2) The dilemmatic situation is _realistic_, i.e., can be reasonably expected to arise even in a small, but non-negligible, number of events.
3) _Avoid ethically-clear scenarios_, i.e., scenarios where an ethical principle would clearly have the highest priority (e.g., safety would clearly be prioritized against all other principles in a medical context). The scenarios were crafted to `neutralize' principles with expectedly high priority, so that none of the remaining principles is intuitively more important than the others.
4) Identify test scenarios in _different application contexts_, so that the examined LLMs could be tested for different context- and sector-specific prioritization.

# Synthesized ethical dilemmas
Based on the above criteria, five hypothetical scenarios were constructed to examine how LLMs treat ethical dilemmas. 
The first scenario is a variation of the trolley problem, where the safety impact is equal in both possible decisions. In addition, both parties (passenger and pedestrian) have violated a safety rule. The goal is to test how LLMs interpret concepts such as duty of care, implied contractual obligations, risk distribution, and moral accountability in autonomous vehicle decision-making.

The second scenario contrasts user privacy rights vs corporate sustainability in a high-impact cybersecurity incident, enabling analysis of AI responsibility, stakeholder prioritization and trade-offs in  cybersecurity. The goal is to examine whether the tested LLMs will prioritize customer privacy, corporate resilience, or strategic regulatory risk minimization.  

The third dilemma involves finance and in particular, AI-assisted investment systems. The goal is to examine the effect of ethical principles when clients' financial goals may contradict social responsibility or long-term ethical impact.

The fourth dilemma is from the health sector and examines the ethical concerns when patients' efficiency is set against hospitals' resource allocation. 

Finally, the fifth dilemma combines two sectors already examined in isolation in the previous scenarios:  autonomous vehicles and the health sector. However, it examines the effect of ethical principles in environmental optimization vs social equality and resource optimization. 

## Experimental setup
For each scenario, a set of questions was constructed to test the ethical behavior of the examined LLMs. In all cases, the first question (Q1) asks the examined LLMs to choose one of the two options provided for each ethical dilemma. The goal is to examine the responses of the tested LLMs, and in particular the consistency of the responses within each model, i.e., the ethical prioritization→decision mapping (how “strong" is the enforcement of the applied ethical model in each LLM), as well as the convergence across LLMs, without modifying their internally set priorities. Then we asked each model to reconsider its decision after we explicitly prioritized specific ethical principles (Q2–Q5). We distinguished two categories. First, we examine the effect of eclectic ethical models (questions Q2 and Q3), where specific ethical principles are prioritized. In the case of Q2, for each scenario, allegedly contradicting ethical priorities were deliberately chosen to provoke ethical confusion. In the case of Q3, the ethical principles were deliberately chosen to be consistent with each other for the specific context. In the second category (questions Q4 and Q5), we chose pure ethical frameworks (Kantian ethics in Q4 and Utilitarianism in Q5). The goal was to test the
effect of diverse ethical prioritization frames in LLMs and to examine the sensitivity (consistency, decision flipping and convergence) of their ethical reasoning. Finally, in all scenarios the last question (Q6) is a repetition of the initial query. The goal here was to examine the consistency of the ethical models of each LLM within a single chat, i.e., whether LLMs have strong ethical beliefs based on their ethical training. For all scenarios, all questions were manually repeated in four runs using different user accounts. Instead of automatically running a large number of prompt repetitions, we deliberately chose a smaller number of manual repetitions from different user accounts. The goal here was to examine the convergence or divergence on the decisions chosen by the LLMs, after removing possible biases related with the prompt history of a single user. 

## Ethical reasoning for the definition of ethical prioritizations
Bearing in mind the debates on so-called “Principlism”, introduced by Beauchamp and Childress (1979), we focus on the four main principles of Bioethics for methodological and practical purposes. Without fully endorsing the view that these principles are derived from (or correspond to) contradictory ethical theories, we acknowledge that, when implemented, they often lead to conflicts. Therefore, we take the principles of beneficence and non-maleficence as representing consequentialist ethical theories -more concretely, as corresponding to classic utilitarianism- whereas the principles of autonomy and justice are conceived as representing deontological views due to their adherence to rules. Under these considerations, we examine the “eclecticism hypothesis” of the LLMs' reasoning and behavior (reflecting their initial ethical training) by experimenting on whether, and under which conditions, a consistent and coherent resolution of these conflicts might emerge.
In this purposefully simplified way, we employ the most common conflicts between “utilitarian” and “deontological” principles (e.g., autonomy vs. beneficence, autonomy vs. non-maleficence etc.) in the Q2 scenarios, to highlight how LLMs perceive ethical dilemmas and inconsistencies and how they arbitrate such conflicts. We anticipate that the responses to these provocative scenarios, through the prioritization of utilitarian- or deontological-oriented argumentation, will reveal the limits of the LLMs' ethical reasoning and whether these models can move beyond ethical dichotomies. After assessing their “ethical sensitivity” in marginal circumstances, we proceed to further verify it by pairing and comparing more compatible and interrelated principles in the Q3 scenarios. By employing these more nuanced and moderate scenarios, we examine the ability of LLMs to prioritize -or identify inconsistencies between- fundamental and procedural ethical principles stemming from the same ethical framework. 

## Scenario 1: ....


## Scenario 2: ...


## Scenario 3: ...


## Scenario 4: ...


## Scenario 5: ...




