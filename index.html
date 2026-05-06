import streamlit as st
import pandas as pd
import plotly.express as px

# -------------------------------
# Page Configuration
# -------------------------------
st.set_page_config(
    page_title="HR Attrition Dashboard",
    page_icon="📊",
    layout="wide"
)

st.title("📊 HR Attrition Analysis Dashboard")
st.markdown("Interactive Employee Attrition Insights")

# -------------------------------
# Load Dataset
# -------------------------------
@st.cache_data
def load_data():
    df = pd.read_csv("HR_Attrition_10000_Employees.csv")
    return df

df = load_data()

# -------------------------------
# Sidebar Filters
# -------------------------------
st.sidebar.header("🔎 Filter Data")

department = st.sidebar.multiselect(
    "Select Department",
    options=df["Department"].unique(),
    default=df["Department"].unique()
)

gender = st.sidebar.multiselect(
    "Select Gender",
    options=df["Gender"].unique(),
    default=df["Gender"].unique()
)

overtime = st.sidebar.multiselect(
    "Overtime",
    options=df["OverTime"].unique(),
    default=df["OverTime"].unique()
)

filtered_df = df[
    (df["Department"].isin(department)) &
    (df["Gender"].isin(gender)) &
    (df["OverTime"].isin(overtime))
]

# -------------------------------
# KPI Section
# -------------------------------
st.subheader("📌 Key Metrics")

col1, col2, col3, col4 = st.columns(4)

total_employees = len(filtered_df)
attrition_rate = (filtered_df["Attrition"] == "Yes").mean() * 100
avg_salary = filtered_df["MonthlyIncome"].mean()
avg_years = filtered_df["YearsAtCompany"].mean()

col1.metric("Total Employees", total_employees)
col2.metric("Attrition Rate (%)", f"{attrition_rate:.2f}")
col3.metric("Average Salary (₹)", f"{avg_salary:,.0f}")
col4.metric("Avg Years at Company", f"{avg_years:.1f}")

st.divider()

# -------------------------------
# Charts Section
# -------------------------------

# 1️⃣ Attrition by Department
st.subheader("📍 Attrition by Department")
fig1 = px.histogram(
    filtered_df,
    x="Department",
    color="Attrition",
    barmode="group",
    title="Department vs Attrition"
)
st.plotly_chart(fig1, use_container_width=True)

# 2️⃣ Salary Distribution
st.subheader("💰 Salary Distribution")
fig2 = px.histogram(
    filtered_df,
    x="MonthlyIncome",
    color="Attrition",
    nbins=30,
    title="Salary Distribution by Attrition"
)
st.plotly_chart(fig2, use_container_width=True)

# 3️⃣ Years at Company vs Attrition
st.subheader("📅 Years at Company vs Attrition")
fig3 = px.box(
    filtered_df,
    x="Attrition",
    y="YearsAtCompany",
    color="Attrition",
    title="Tenure vs Attrition"
)
st.plotly_chart(fig3, use_container_width=True)

# 4️⃣ Overtime Impact
st.subheader("⏳ Overtime Impact on Attrition")
fig4 = px.histogram(
    filtered_df,
    x="OverTime",
    color="Attrition",
    barmode="group",
    title="Overtime vs Attrition"
)
st.plotly_chart(fig4, use_container_width=True)

# -------------------------------
# Download Option
# -------------------------------
st.download_button(
    label="📥 Download Filtered Data",
    data=filtered_df.to_csv(index=False),
    file_name="Filtered_HR_Data.csv",
    mime="text/csv"
)

st.success("Dashboard Loaded Successfully ✅")
