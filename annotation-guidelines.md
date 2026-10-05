# Project: Detecting Premature Problem Solving in Mental Health Counseling Responses

**Annotation Guidelines and Interface**

**Task Overview**

Your task is to review a pair consisting of a **Context** and a **Response**.  You will evaluate whether the response properly validates the user's emotions before jumping into solutions.

**Labeling Criteria**

* **Select YES if:**  
  * The response **first** validates or acknowledges the user's feelings, distress, or emotional state.  
  * **Then**, it transitions into providing advice, action steps, recommendations, diagnosis, treatment, or guidance.  
* **Select NO if:**  
  * The response **immediately** jumps into advice, action steps, recommendations, diagnosis, treatment, or guidance **without** first acknowledging the emotional concern.  
    

| Rule | Classification |
| ----- | :---: |
| The response adequately acknowledges the emotional concern before moving into advice/action/recommendation/diagnosis/treatment/other solution or directed guidance | YES |
| The response moves into advice/action/recommendation/diagnosis/treatment/other solution or directed guidance before adequately acknowledging the emotional concern | NO |

 

**Examples of YES Label**
<img width="1630" height="372" alt="image1" src="https://github.com/user-attachments/assets/3783449d-cf0f-4353-9ed2-9538f54c34d1" />


**Examples of NO Label**
<img width="1627" height="392" alt="image2" src="https://github.com/user-attachments/assets/ef121876-a391-463d-af4d-8de8c5b9caf3" />
