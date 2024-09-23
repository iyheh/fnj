import streamlit as st
from transformers import pipeline

st.title("텍스트 감정 분석")

# 감정 분석 파이프라인 불러오기
sentiment_analysis = pipeline("sentiment-analysis")

# 사용자 입력 받기
text = st.text_area("분석할 텍스트를 입력하세요")

if st.button("감정 분석 실행"):
    if text:
        # 감정 분석 실행
        result = sentiment_analysis(text)[0]
        st.write(f"분석 결과: **{result['label']}** (점수: {result['score']:.2f})")
