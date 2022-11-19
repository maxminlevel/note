# Proof of stakes

Leader gửi block cho các validator, sau khi được validate xong thì block đó được broadcast to chain.

PAXUS

BFT
pBFT
hot stuff
raft

3 phase:
- P1: Gửi block đến các validator
- P2: Listen nhận file và validate sau đó gửi kết quả
- P3: Nhận kết quả và gửi lại block + list vote 

- P3': Thay vì giữ connection từ master đến mọi node thì node validate broadcast giảng

? Case: Chỉ nhận được 1/3 vote không nhận đủ [2/giảng