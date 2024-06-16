# Google Cloud Platform Project
#### 🧊 Getting big data with Storage Bucket, Compute Engine API, Dataproc (Apache Hadoop and Spark), and BigQuery

GCP Project
Account Setup
1.	Go to cloud.google.com. Create a Google Account/Sign-In with a Google Account.
2.	Towards the upper-left side, near the Google Cloud logo, Click the Box.
3.	A dialog box will open, click the box in the upper-right corner, “New Project.”

## Storage Bucket Setup
 4.	Select the navigation menu (hamburger icon) in the upper right corner; Hover over Cloud Storage; Select Buckets
 5.	Enter the following information: Storage Bucket name, storage location, storage class (default), storage control access (e.g., public access prevention, and uniform access control), storage object data (e.g., soft delete policy, object versioning, bucket retention policy, object retention, encryption type). Click create.
## Compute Engine API Setup
 6.	Select the navigation menu (hamburger icon) in the upper right corner: hover over APIs and Services; Select “Enable APIs & Services”
7.	Select “+ ENABLE APIS AND SERVICES”
8.	Scroll down until you find “Compute Engine API” under Google Enterprise APIs; Select “Compute Engine API”.
9.	Select “Enable” on the Compute Engine API product details page.
## DataProc Setup
10.	Select the hamburger icon in the upper right corner; Hover over Dataproc; Click/Select Dataproc
11.	You will be directed to the Cloud Dataproc API product details page. Select “Enable” to enable Dataproc API – This will enable Hadoop Clusters for big data.
## DataProc Cluster Creation
12.	Directed to Dataproc Cluster Page. Select CREATE CLUSTER
13.	Select CREATE to Create a Cluster on the Compute Engine
14.	Enter the following information: Name, Select Region, Zone, Cluster type: Standard (1 master, N workers)
15.	Select Change to change the release date. This allows you to change the version images to a specific OS bundle of your choice. For this project, we will be sticking with Debian 12; however, Ubuntu 12 or Rocky Linux are good alternatives.
16.	Select Configure nodes in the left-hand menu; Create a Dataproc cluster and its manager and worker nodes on the compute engine using the following information:
a.	Crete a name
b.	Under the Machine family GENERAL –PURPOSE tab
c.	Select Series: E2 (for basic).
d.	Select Machine type: e2-standard-4 (4 vCPUs, 16 GB memory) as standard or basic computation.
e.	 Enter Primary disk size 128 GB
f.	Select Primary disk type: Standard Persistent Disk
g.	 Scroll down to the worker nodes
17.	Select Configure nodes in the left-hand menu; Create a Dataproc cluster and its manager and worker nodes on the compute engine using the following information:
a.	Crete a name
b.	Under the Machine family GENERAL –PURPOSE tab
c.	Select Series: E2 (for basic).
d.	Select Machine type: e2-standard-4 (4 vCPUs, 16 GB memory) as standard or basic computation.
e.	 Enter Primary disk size 128 GB
f.	Select Primary disk type: Standard Persistent Disk
g.	 Scroll down to the worker nodes
18.	Select Customize cluster
19.	Scroll down to “Cloud Storage staging bucket” and Select Browse.
20.	Find the storage bucket you created [storage bucket name]
21.	Select your bucket and then Click SELECT
22.	After you’ve verified that you can see your storage bucket, select CREATE. Wait for the provisioning of your cluster.
23.	Your new Hadoop cluster HAS BEEN CREATED SUCCESSFULLY and IT IS RUNNING.
NOTE: If you intend to use your cluster immediately after creation, then allow it to run, but if not, stop the cluster by ticking the box next to the cluster and selecting “STOP.”
## Running VM Instances
24.	Select the Navigation Menu (hamburger icon menu), scroll down to Compute Engine and Select VM instances
25.	 Select the arrow next to SSH of the manager node to expand a drop-down menu
26.	Select “Open in a browser window”
27.	Select Authorize
a.	Note: It takes several seconds for the authentication to be done so wait patiently
28.	After authentication, an SSH terminal will pop up in the browser.
a.	Note: Utilizing GCP documentation will allow you to become knowledgeable about how to use OpenSSH, PuTTY app, or Secure Shell Chrome App to SSH GCP VM into your local network.
## BigQuery
29.	 Enable BigQuery API Verify BigQuery API is enabled; if not, you need to enable the API now. Type in BigQuery API in the search bar and click on BigQuery API under Marketplace results (NOT Documentation results). Then click Enable if it is not enabled.
30.	Step 2: Find the public dataset 2.1 Go to the Navigation Menu and Select BigQuery and BigQuery Studio. If a Welcome screen opens, read it, and select DONE. Next, in the Type to search field, enter a desired public data and ENTER or click SEARCH ALL PROJECTS if nothing displays or “ + ADD” next to “Explorer to add your dataset. For this project, I will connect the storage bucket data.
31.	Out of Local File, Google Cloud Storage, and Connections to external data sources, Select “Google Cloud Storage.” If the dataset you want to use is somewhere else, scroll down and find the appropriate selection.
32.	In the Create table menu under Source:
a.	Select Google Cloud Storage from Create Table Form (or wherever your dataset is based)
b.	In the “Select file from GCS bucket,” select Browse.
i.	Select the desired storage bucket from the storage bucket file selection (i.e., Elden-ring-ultimate-bucket)
ii.	Choose the desired individual file from the storage bucket (e.g., bosses.csv)
iii.	Click Select
c.	For file format, select the format according to your dataset. I selected CSV.
33.	In the Create Table menu under Destination:
a.	Leave the name in Project the same to create consistency.
b.	Select dataset, open Create Dataset menu.
i.	Enter dataset ID/name
ii.	Select region (typically multi-region)
iii.	Leave Default table expiration and tags alone for the moment.
iv.	 Make sure Google Encryption is selected under advanced options
v.	Click Create Dataset
vi.	Enter Table name (like dataset to keep consistency) (e.g., elden_ring_bosses.
vii.	Since we are using a dataset from Google Cloud Storage, choose Native Table under Table type. If we were using an external dataset, we would’ve chosen External Table.
34.	In the Create Table menu under Schema, Select Auto-detect, unless you want to fine-tune the dataset’s schema.
35.	Leave Partition and cluster settings, Tags, and Advanced Options alone (advanced topics for a later date).
36.	Select Create Table.
37.	The table is now viewable and can be edited or queried
a.	NOTE: TO add another dataset to the project, repeat the same steps.
Exploring and Querying BigQuery Datasets (Coming Soon with SQL Tutorial)

