# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
import pandas as pd import seaborn as sns import matplotlib.pyplot as plt df=pd.read_csv("titanic_dataset.csv") df.head()
<img width="1032" height="178" alt="530486659-dcd20cea-0acd-424d-9be7-33d4ee28f59e" src="https://github.com/user-attachments/assets/b4a7caf0-376f-46da-83c1-ff25edf182a5" />
x=[1,2,3,4,5] y=[3,6,2,7,1] sns.lineplot(x=x,y=y) plt.title('Line Plot')
<img width="659" height="533" alt="530486671-57847684-d1be-4dc2-ba17-9bfbeb8e97d8" src="https://github.com/user-attachments/assets/dc1ddc31-9c1c-4b1f-a24f-c9aeba2669ce" />
x=[1,2,3,4,5] y1=[3,5,2,6,1] y2=[1,6,4,3,8] y3=[5,2,7,1,4] sns.lineplot(x=x,y=y1) sns.lineplot(x=x,y=y2) sns.lineplot(x=x,y=y3) plt.title('Multi Line Plot')
<img width="664" height="536" alt="530486695-2394c2dd-e6fd-4f03-b0e7-9b75e38d740f" src="https://github.com/user-attachments/assets/b45ad2b3-c118-4e49-8d7a-cd59579a5820" />
plt.figure(figsize=(8,5)) sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow') plt.title("Fare Of Passenger By Embarked Town") 
<img width="846" height="579" alt="530486717-8f3e9f3d-c56b-44a5-9728-b579cd1007f6" src="https://github.com/user-attachments/assets/57286307-e293-428c-a779-cf746edd37dc" />
sns.scatterplot(x="Age", y="Fare", data=df) plt.title('Scatterplot of Age vs Fare') plt.show()
<img width="703" height="549" alt="530486731-0077d544-32ab-416f-87e7-670cc1badcf4" src="https://github.com/user-attachments/assets/3a5c01ab-3699-40d6-b2f5-b1b179002b8d" />
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200)) plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class') plt.show() 
<img width="706" height="551" alt="530486750-c2826262-9b4b-4107-a128-83b48efee60f" src="https://github.com/user-attachments/assets/e5a2ac16-c0d0-488a-bbc1-1e8709c07587" />

ns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
<img width="571" height="432" alt="530486771-a9af838b-b62e-4b1e-9369-a6dc33316532" src="https://github.com/user-attachments/assets/c1fd0fc6-ffa5-4db9-b1dd-f437c2327165" />
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow') plt.title("Age By Passenger Class")<img width="684" height="550" alt="530486790-3c192977-6711-4027-968b-02887a9d323a" src="https://github.com/user-attachments/assets/2ff3a93e-8e82-4324-afd3-4e0c0820b444" />
sns.violinplot(x="Pclass", y="Fare", data=df) plt.title('Violin Plot of Fare by Passenger Class')
<img width="571" height="453" alt="530486808-87b239e1-0ccd-44da-88dd-a8fd1ace47dc" src="https://github.com/user-attachments/assets/8420af40-ca3f-4510-a3d0-eb83233fa751" />
sns.kdeplot(data=df['Age'], shade=True) plt.title('Density Plot of Passenger Ages') plt.show()
<img width="723" height="551" alt="530486823-72eedd8a-6318-46c6-b507-08be4af98e5f" src="https://github.com/user-attachments/assets/1df101f6-c455-4347-85ce-87f646247652" />
numeric_df = df.select_dtypes(include=['float64', 'int64']) corr_matrix = numeric_df.corr() sns.heatmap(corr_matrix, annot=True, cmap='coolwarm') plt.title('Heatmap of Titanic Dataset') plt.show()
<img width="730" height="614" alt="530486836-93c32702-8c77-4eb1-86e7-0537869510db" src="https://github.com/user-attachments/assets/b1b2ce1b-c98b-42ec-bc5c-4fc23dad7a5f" />
# Result:
 Thus,the Data Visualization using seaborn python data is implemented successfully
