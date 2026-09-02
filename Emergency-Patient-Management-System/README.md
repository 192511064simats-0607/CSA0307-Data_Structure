# Emergency Patient Management System

The Emergency Patient Management System (EPMS) is a web-based application developed to manage patients in a hospital emergency department in an efficient and organized manner. The main purpose of the system is to ensure that patients who require immediate medical attention are given priority over patients with less severe conditions.

In a traditional First-In-First-Out (FIFO) queue, patients are treated based only on their arrival time. This approach is not suitable for an emergency department because a patient with a critical condition may arrive after a patient with a less serious condition. If the normal FIFO method is followed, the critical patient may have to wait longer for treatment.

To overcome this problem, the Emergency Patient Management System uses a **Priority Queue** data structure. Each patient is assigned a priority according to the severity of their condition. Critical patients are given the highest priority, followed by Severe, Moderate, and Mild patients.

The priority levels used in the system are:

**Critical → Priority 1**  
**Severe → Priority 2**  
**Moderate → Priority 3**  
**Mild → Priority 4**

A lower priority number represents a higher treatment priority. Therefore, a Critical patient will be considered before a Severe patient, while a Severe patient will be considered before a Moderate or Mild patient.

The system also considers the arrival order of patients. When two or more patients have the same severity, the patient who arrived earlier is treated first. This combines the advantages of a Priority Queue and FIFO ordering. It ensures that emergency situations are handled according to severity while maintaining fairness among patients with equal severity.

The application provides a simple interface through which hospital staff can register new patients and enter important details such as patient ID, patient name, arrival time, assigned doctor, and severity. Once the patient is registered, the system automatically assigns the appropriate priority and places the patient in the emergency queue.

The emergency queue continuously displays patients according to their treatment priority. The patient at the front of the queue represents the next patient who should be treated. When the treatment operation is performed, the highest-priority patient is removed from the waiting queue and marked as treated. The treatment time is recorded, and the patient's information is transferred to the treatment history.

The system also allows patient information to be searched easily. This helps staff locate a patient's details without manually checking the complete queue. Treatment history provides a record of patients who have already received treatment.

A dashboard is included to provide an overall view of the emergency department. It helps display information about the total number of patients, waiting patients, critical patients, treated patients, and the next patient in the queue.

The system uses **LocalStorage** to maintain patient and treatment information within the browser. This allows the stored information to remain available even when the webpage is refreshed.

The project demonstrates the practical application of data structures in a real-world healthcare scenario. The use of a Priority Queue makes the system more suitable for emergency patient management than a simple FIFO queue because it considers the urgency of each patient while also maintaining arrival order for patients with the same severity.

Overall, the Emergency Patient Management System provides a simple, organized, and efficient approach to emergency patient queue management. The project demonstrates how an appropriate data structure can be used to solve a real-world problem and improve the efficiency of patient treatment management.
