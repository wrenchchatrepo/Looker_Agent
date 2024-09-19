# How to Use the Signed URLs for Each Bucket
Each signed URL you generated allows temporary access to a specific file in your buckets. Below are instructions for users on how to use these URLs based on the bucket content type.
## 1. Accessing Multiple Files in a Bucket (e.g., bigquery/, help_docs/, looker_studio/, repo_docs/)
+ Since these folders contain multiple files, you’ll need to generate individual signed URLs for each file users want to access. For users to access these files:
### Example Instructions for Users:
1. Receive Signed URLs:
+ You will be provided with multiple signed URLs for each file you need to access in these folders.
2. Open Each URL:
+ Copy and paste each signed URL into your browser’s address bar.
+ Press Enter to download or view each file.
3. Manage Multiple Downloads:
+ You can use a download manager or save each file manually if you have many URLs to access.
4. Automate with a Script:
+  If you have many files, you can provide a script using curl commands to download all files at once. For example:
```
curl -O "https://storage.googleapis.com/agent_miguel_looker_bucket/bigquery/file1.txt?x-goog-signature=..."
curl -O "https://storage.googleapis.com/agent_miguel_looker_bucket/bigquery/file2.txt?x-goog-signature=..."
```
## 2. Accessing a Single Large File (e.g., doit_looker_agent_bucket/, tickets/)
+ These buckets have a single large file like a zip or CSV, making it easier to access.
### Example Instructions for Users:
1. Receive the Signed URL:
+ You will get a single signed URL to access the file.
2. Open the URL:
+ Copy the signed URL and paste it into your browser’s address bar.
+ Press Enter to start the download.
3. Download the File:
+ The browser will either start downloading the file automatically or prompt you to save it.
4. Extract or View the File:
+ For a ZIP file, extract the contents after downloading.
+ For a large CSV file, open it with a spreadsheet application like Excel or Google Sheets.
3. Sample URLs for Each Bucket
+ Here are the signed URLs for reference. Users can simply click or copy these into their browser to download or view the files.
1. BigQuery Files:
```
https://storage.googleapis.com/agent_miguel_looker_bucket/bigquery/test.txt?x-goog-signature=4b412f28b4829af9aa2c4e0137e7112584bbf9bd7370b97c2038845df59649ec3d08832f9ad4d6ac419bcc9a2c4c08f7d4df3357bb6d4f48253d03994ee99d8482d70e99e4d6e94d1d1e7927c0b445bb2a283205fe8606436a2f47b55aabcea2fc054057fb6779ebe3af5a0d8790d50aa7975bf9a5c0e1b5ec756919e11ebf13d89b055fc4e96c522808861db4b1d9332719ac01e77b3c1601a05b6bce6eb5da9129681b2fcc5fc90c24e7adc5426b487d39cdb1e37acdd21a9d1d53013daab9e69d919fc86c2717e2cb4b2c37dd1cb4f0a5f7b6a051d3bc4e43af737232f7c80853beb49da7d8c30ea43780815c81464956a5a145bea480076588f70e50cf71
```
2. DoIT Looker Agent ZIP File:
```
https://storage.googleapis.com/agent_miguel_looker_bucket/doit_looker_agent_bucket/test.txt?x-goog-signature=08538c709bf50eeeab9c70bf48dad939bc85a93fe2ac136fadf7bbbaed675d9761e01a7708f17dddf54bf5ce4190add7a3f820fc907dce2a35b7ca948ea9772fef4bbd57d29cb9a09a499baf1bc451ae9bd905541d65e467425db1d992035b19760d38152328dbb68c8877e6cf1a63f04d0acd35b094e5b1c746153e8b542fd19dff08cb3b298dc95c74eaef1a7b79bbc7b40029f9f9a4bf13655ede9663524a9b29fcb1f1d21e1623a05fb863040c8937dd5cc54729b0d49de60a582ffef605d01994870ac5fb6d8b14c9043d2c2395012772140eeb593915674ae62fc5196b57611e1908fc94079afd07d89baaa78266dac1863e9d56b4604cac13203124fd
```
3. Help Docs Files:
```
https://storage.googleapis.com/agent_miguel_looker_bucket/help_docs/test.txt?x-goog-signature=10ec3fbca049c4f410074021b2fefc838307fec1735c33e607e72fbcde3b793ea7c7805f5f5e122595629714f079f53be50ede449d8a3dba46e120024a1ef8610dab5ea25b327064096f45537e1e04ade15356cb9cccc874d349c9211d82263d190258b7ff1984041b6acb3f5e3e9386b29e86a21b09a022012da9d15984dc5611b4fac6cc592235085795bff7a804b6d212f2f9d50d7e55eb84239e5d6a57fd682661b29498424dcad73f5c7cdf686b71b1c240e809664ce540446fb88fbe0f9b3817e247000ecb208483c02de1077f2c4c54f95aa8fb112dc9f1628a32c61ad7bec91f5730d5490685aaf15527e9eb6e01614745149335a9bda60fa6ba09d2
```
4. Looker Studio Files:
```
https://storage.googleapis.com/agent_miguel_looker_bucket/looker_studio/test.txt?x-goog-signature=70dc6c37263ddd4cbd8c2172fcde3057820e6a9a35265848fb0081c786d92c8aab917f7b4841576f1c9a61878248375f7e0694ca39425101c8c5f53df6b163269dcb245cabad52b6e3f048d6fd5e389f4eb9d34e70c4ce7018f0f89715dcf074ea43ab78b13e641caf426d46e3621bcde4c1729fb0ca13fbebc0b0e5cf0b10b11471a6e7ade968eda2d5cf9e474590cc9de3c7e1128d549bed2e8774c70c8aadd6dc8a83c509adbcd0b1a2a527d444fc2ee9dbdb8142c8449b12640c8bf049f87dbb23bcdeb59d6ed780a5d92a5abb581dccd161b61b5ca93b41b21bb4fa126290bd20b4b26f03de43f1dbe5474cb14d07d36ed66ba3ca2bd3f6c3d8c5e40342
```
5. Repo Docs Files:
```
https://storage.googleapis.com/agent_miguel_looker_bucket/repo_docs/test.txt?x-goog-signature=0e51f0354b2bfdf8d91c0af06aa9347c5cbf83d3aedb12f6fa882eb911877055cf727c65f0736a45cc189434538b93838e43b9ba2bb9761eee6ca55441970489c7b609bf7dd44cf2b2ad3d54c1076759763ea3dbd1e16a94c0a64dbe1d01aef451e2807dbd6e47e2719b521f6b27c4e1ffdfd90d87cfbf629742596a5b5b4cc16a7c3bb5543d5d4eef8acbc0e30c63d52f6254c24ca168037817ce9abdde67304ebd4232410e5d063567688e188a300b3516d269b381417de9b8c32d0d912d9939d3fd472a7bbfe878122ec5324afdee79512c30f266aed5b927163885a819be0fe0eb7f632209c4dbf1bb94002e63a00f52da97f6bb969533e9cc54f6a7d297
```
6. Tickets:
```
https://storage.googleapis.com/agent_miguel_looker_bucket/tickets/test.txt?x-goog-signature=7870cdca1690862ccb9ff1cd9bff6cb807116d6253b256662bd1704e37cbbd6479a06fc159c3e2ea98fe5b1d14ded8f7302be857d2b82389f98dacbbbd286d55504017cdd3d0b08f7e5b051c47d2b9b5017fc1e54e4f607fadac1da8a23093317b72232937dec3709dbab23eb4210caeb760c6ea71197ef835c6410e49d3933e934ed73434ce1a10a3a3f3674c3d93d45a3f907af82791029ec2577603baeb02dd697ac18ed15ec2ec33e52b16778cb1e32bf6d04811563b66a25707e9c214e2581b0e9f833e032efbf27716d9717ffb2f659da1080fcea41a385d0b716510e2216fadaf3401f291990d8cb82989254f8099d6fe619fb38e70b9fdd811a62a44
```
## Tips for Using the URLs
1. For Browsers: Copy and paste the full URL into the browser address bar and hit Enter.
2. For Scripting: Use curl commands to download files directly to your machine.
3. Valid for 4 Hours: Each signed URL will expire 4 hours from when it was generated.
