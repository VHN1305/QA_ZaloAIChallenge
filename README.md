# QA_ZaloAIChallenge

Dự án này được tôi thực hiện để tạo ra 1 chatbot có thể trả lời được những câu hỏi Tiếng Việt

Dự án gồm 2 phần, phần thứ nhất là nội dung bài toán Question Answering và phần thứ 2 là Reading Comprehension

## Question Answering

Đối với phần QA, đầu vào cho pha huấn luyện sẽ bao gồm câu hỏi và đoạn văn chứa câu trả lời của câu hỏi đó (query - context)
Mô hình sẽ tìm các học để suy diễn context phù hợp nhất với query đầu vào

Đối với pha này, mô hình sẽ bao gồm 2 phần Retrieval Information và Rerank, tôi sử dụng kỹ thuật Finetuning Bert Pretrain Model cho tiếng việt dựa trên bộ dữ liệu ZALO-AI_CHALLENGE 2022.

Dưới đây là 1 demo của pha này
![alt text](image.png)

## Reading Comprehension

Đối với phần này, đầu vào cho pha huấn luyện sẽ bao gồm câu hỏi, đoạn văn chứa câu trả lời và câu trả lời cho câu hỏi (query - context - answer)

Khi suy diễn, query và context sẽ là đầu vào và mô hình sẽ dự đoán câu trả lời cho câu hỏi, Với context chính là đầu ra của pha QA.

Tiếp tục sử dụng kỹ thuật Finetuning Bert Pretrain Model, pha này tôi sử dụng XLMRoberta - mô hình BERT được đào tạo với đa ngôn ngữ và bao gồm cả tiếng việt.

Dưới đây là demo cho phần này:

![alt text](image-1.png)

