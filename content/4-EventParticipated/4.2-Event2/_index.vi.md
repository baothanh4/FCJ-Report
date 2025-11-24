---
title: "Event 2"
date: 2025-09-07
weight: 1
chapter: false
pre: " <b> 4.2. </b> "
---

# Báo cáo Tóm tắt: “Generative AI with Amazon Bedrock”

### Mục tiêu của sự kiện

- Tìm hiểu Amazon Bedrock là gì và các mô hình AI đang được sử dụng
- Học sâu hơn về Prompt Engineering: Zero-Shot, Few-Shot, Chain of Thought (CoT)
- Tìm hiểu Retrieval Augmented Generation và các trường hợp sử dụng RAG
- Khám phá thêm các dịch vụ AI pretrained
- Tìm hiểu Amazon Bedrock AgentCore và xem demo trực tiếp

### Diễn giả

- **Lam Tuan Kiet** – Sr DevOps Engineer, FPT Software  
- **Danh Hoang Hieu Nghi** – AI Engineer, Renova Cloud  
- **Dinh Le Hoang Anh** – Cloud Engineer Trainee, First Cloud AI Journey  

### Các điểm nổi bật
- **Foundation Models**
- **Prompt Engineering**
- **Retrieval-Augmented Generation (RAG)**
- **Bedrock AgentCore**

#### Foundation Models
![Why foundation models](/images/foundation_model.jpg)

| | Mô hình ML truyền thống | Foundation Models |
| --- | ------------------------------------------------------------------ | ---------------- |
| **Mục đích** | Hẹp, chuyên biệt từng tác vụ (classification, regression, forecasting, clustering,...) | Đa dụng, đa miền, đa tác vụ |
| **Dữ liệu huấn luyện** | Thường là dữ liệu structured/tabular hoặc domain-specific | Tập dữ liệu khổng lồ (text, image, code,...) |
| **Yêu cầu huấn luyện** | Phải huấn luyện thủ công với dữ liệu gán nhãn | Không cần — đã được pretrained |
| **Tùy chỉnh** | Cần tinh chỉnh hyperparameter, feature, dataset | Tùy chọn — fine-tuning, RAG, prompt engineering |
| **Ví dụ** | Random Forest, XGBoost, SVM, Linear Regression | Claude, Llama, Cohere Command, Titan |
| **Kỹ năng cần thiết** | Chuyên môn ML cao (feature engineering, training pipeline) | Rất thấp — chỉ cần viết prompt |
| **Dịch vụ AWS** | **SageMaker**, Amazon ML, custom training | Amazon Bedrock, Bedrock Studio |
| **Use cases** | Dự đoán, Forecasting doanh số, Phân loại ảnh, Fraud detection, anomaly detection | Chatbot, Tóm tắt văn bản, Sinh mã, Sinh ảnh, Ứng dụng hội thoại, Tìm kiếm tài liệu với RAG, Sentiment analysis, Dịch đa ngôn ngữ |

Supported foundation models in Amazon Bedrock  
![Supported foundation models in Amazon Bedrock](/images/supported_foundation.jpg)

---

#### Prompt Engineering - Tạo và tinh chỉnh hướng dẫn (prompt)

#### Prompt là gì?

- Là đầu vào bạn cung cấp cho mô hình AI (như ChatGPT, Claude, Gemini, hoặc các mô hình trên Amazon Bedrock) để nhận được đầu ra mong muốn.

#### Ví dụ
![Example](/images/example_prompt.jpg)

---

### Sự khác nhau giữa Zero-Shot, Few-Shot và Chain of Thought trong Prompting Techniques

| Kỹ thuật | Mô tả | Khi nào dùng | Ưu điểm | Hạn chế | Ví dụ |
|---------|-------|--------------|---------|---------|-------|
| **Zero-Shot** | Model chỉ nhận instruction, **không có ví dụ mẫu** | Nhiệm vụ đơn giản; model đã quen miền kiến thức | Prompt ngắn, nhanh, không cần chuẩn bị nhiều | Chính xác thấp với tác vụ phức tạp | "Hãy phân loại đoạn văn thành neutral, negative hoặc positive." |
| **Few-Shot** | Cung cấp **một vài ví dụ** để dạy model pattern | Yêu cầu output theo format riêng; tác vụ theo mẫu | Chính xác cao hơn; model học phong cách bạn muốn | Prompt dài hơn; tốn token | Ví dụ có mô tả về "whatpu" |
| **Chain-of-Thought** | Yêu cầu model **giải thích từng bước** | Bài toán logic, toán, code, multi-step | Lý luận tốt hơn, output chính xác hơn | Chậm hơn; trả lời dài | "Hãy cho thấy từng bước suy luận." |

---

### Retrieval Augmented Generation (RAG)

#### RAG là gì?

- **Retrieval**: Truy xuất dữ liệu liên quan từ nguồn ngoài (database, document store, API,…)  
- **Augmentation**: Thêm ngữ cảnh vào prompt gửi cho mô hình  
- **Generation**: Mô hình trả lời dựa trên ngữ cảnh đã bổ sung  

#### Use cases RAG

- **Cải thiện chất lượng nội dung**: giảm hallucination, dùng kiến thức cập nhật  
- **Chatbot theo ngữ cảnh**: tích hợp dữ liệu doanh nghiệp  
- **Tìm kiếm cá nhân hóa**  
- **Tóm tắt dữ liệu real-time**  

![RAG](/images/RAG.jpg)

---

### Embeddings là gì?

- Biểu diễn văn bản dưới dạng vector số
- Giúp mô hình hiểu ngữ nghĩa và mối quan hệ giữa các từ  
- So sánh độ tương đồng giữa các đoạn văn  
- Hỗ trợ đa ngôn ngữ  

#### Amazon Titan Embedding
![Amazon Titan Embedding](/images/amazon_titan.jpg)

**RAG in Action**
![Amazon in Action](/images/RAG_Action.jpg)

**Data Ingestion Workflow**
![Amazon ingestin workflows](/images/ingestion.jpg)

**RetrieveAndGenerate API**
![RetrieveAndGenerate API](/images/retrieveAPI.jpg)

---

### Các dịch vụ AI Pretrained khác

![Amazon translate](/images/z7226100700576_8c6d6f4fb782f49cefb3ad8c11c77db2.jpg)

![Amazon Textract](/images/z7226100718462_385f2bde80fcd61d9e5ee0d6b7732f89.jpg)

![Amazon transcribe](/images/z7226100740453_ea3987164a7d69381c4e298f2e847a9b.jpg)

(hình ảnh Amazon Polly)  
![Amazon Polly](/images/z7226100772259_db269fba041e5507e412175ec3a85b34.jpg)

(hình ảnh Amazon Comprehend)  
![Amazon Comprehend](/images/z7226100734521_f068686a3d3c479dc00272d1eb50ad55.jpg)

(hình ảnh Amazon Kendra)  
![Amazon Kendra](/images/z7226100721932_43e82f26dd0532d8525087fd96929c74.jpg)

(hình ảnh Amazon Lookout Family)  
![Amazon Lookout Family](/images/z7226100739536_2c2b097cf02df57d39fe18d3e11318c0.jpg)

(hình ảnh Amazon Personalize)  
![Amazon personalize](/images/z7226100780833_f24a38ebe15aa1e900bcaae88aa94538.jpg)

---

### Amazon Bedrock AgentCore

#### Sự phát triển của Agentic

- **Generative AI assistants**: theo quy tắc có sẵn, tự động hoá tác vụ lặp lại  
- **Generative AI agents**: đạt mục tiêu, xử lý tác vụ rộng hơn, tự động hoá quy trình hoàn chỉnh  
- **Agentic AI systems**: đa agent, tự điều phối, mô phỏng tư duy con người  

#### Framework xây dựng agent

- Strands agents SDK  
- Langgraph, Langchain  
- OpenAI Agents SDK  
- Crew.AI  
- Google ADK  
- LlamaIndex  

#### “Vực sâu” từ prototype → production  
![protype](/images/z7226100812733_a380cf409ce7a61e17eb568bf9305dd3.jpg)

---

### AgentCore — giải pháp giúp agent vận hành ở quy mô lớn

![Agent scale](/images/z7226100823612_1879c44a5cfd3d4dc19e10c65af04445.jpg)

---

### Trải nghiệm Sự kiện (Event Experience)

Tham dự workshop **“Generative AI with Amazon Bedrock”** mang lại nhiều giá trị giúp tôi hiểu sâu hơn cách AI hiện đại và các công nghệ cloud được ứng dụng trong thực tế.

#### Học hỏi từ chuyên gia
- Diễn giả chia sẻ các tình huống thực tế về ứng dụng AI trong doanh nghiệp  
- Hiểu vì sao foundation models, RAG và agentic workflow quan trọng đối với scalability  

#### Trải nghiệm kỹ thuật thực hành
- Học trực tiếp về Zero-Shot / Few-Shot / Chain-of-Thought  
- Demo RAG giúp thấy rõ cách giảm hallucination  
- Quan sát Bedrock AgentCore vận hành tool, lập kế hoạch, xử lý quy trình  

#### Hiểu thêm về hiện đại hóa hệ thống
- Nắm rõ sự khác nhau giữa ML truyền thống và foundation models  
- Hiểu các mô hình hiện đại hóa như Event-driven Architecture, DDD, AI-augmented workflows  

#### Khám phá công cụ AI hiện đại
- Titan Embedding, Textract, Comprehend, Kendra, Polly…  
- Amazon Q Developer hỗ trợ coding, debugging, refactoring  

#### Mở rộng kết nối
- Giao lưu với cloud engineers, AI specialists, developers  
- Hiểu thêm các use cases thực tế trong doanh nghiệp  

#### Những điều rút ra
- RAG là chìa khóa cho AI doanh nghiệp  
- Prompt engineering rất quan trọng  
- Agentic AI là tương lai của workflow automation  
- Hiện đại hoá hệ thống cần roadmap rõ ràng + đo lường ROI  
- AI trong developer workflow tăng năng suất đáng kể  
