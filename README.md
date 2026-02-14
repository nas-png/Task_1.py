

students = [
    {
        "student_id": "S001",
        "records": [
            {"term": "1-2025", "english": 78, "mathematics": 65, "kiswahili": 82, "science": 71},
            {"term": "2-2025", "english": 81, "mathematics": 72, "kiswahili": 79, "science": 68},
            {"term": "3-2025", "english": 85, "mathematics": 78, "kiswahili": 84, "science": 75},
        ]
    },
    {
        "student_id": "S002",
        "records": [
            {"term": "1-2025", "english": 92, "mathematics": 88, "kiswahili": 95, "science": 90},
            {"term": "2-2025", "english": 89, "mathematics": 91, "kiswahili": 93, "science": 87},
        ]
    },
    {
        "student_id": "S003",
        "records": [
            {"term": "1-2025", "english": 64, "mathematics": 58, "kiswahili": 70, "science": 62},
            {"term": "2-2025", "english": 68, "mathematics": 63, "kiswahili": 74, "science": 67},
            {"term": "3-2025", "english": 72, "mathematics": 69, "kiswahili": 78, "science": 71},
        ]
    },
    {
        "student_id": "S004",
        "records": [
            {"term": "1-2025", "english": 55, "mathematics": 72, "kiswahili": 48, "science": 61},
            {"term": "2-2025", "english": 62, "mathematics": 68, "kiswahili": 55, "science": 65},
        ]
    },
    {
        "student_id": "S005",
        "records": [
            {"term": "1-2025", "english": 88, "mathematics": 95, "kiswahili": 84, "science": 92},
            {"term": "2-2025", "english": 91, "mathematics": 89, "kiswahili": 88, "science": 94},
        ]
    },
    {
        "student_id": "S006",
        "records": [
            {"term": "1-2025", "english": 76, "mathematics": 81, "kiswahili": 79, "science": 74},
            {"term": "2-2025", "english": 74, "mathematics": 77, "kiswahili": 82, "science": 70},
        ]
    },
    {
        "student_id": "S007",
        "records": [
            {"term": "1-2025", "english": 45, "mathematics": 52, "kiswahili": 38, "science": 49},
            {"term": "2-2025", "english": 51, "mathematics": 58, "kiswahili": 44, "science": 53},
        ]
    },
    {
        "student_id": "S008",
        "records": [
            {"term": "1-2025", "english": 83, "mathematics": 79, "kiswahili": 86, "science": 81},
            {"term": "2-2025", "english": 87, "mathematics": 84, "kiswahili": 89, "science": 85},
        ]
    },
    {
        "student_id": "S009",
        "records": [
            {"term": "1-2025", "english": 96, "mathematics": 93, "kiswahili": 97, "science": 94},
        ]
    },
    {
        "student_id": "S010",
        "records": [
            {"term": "1-2025", "english": 71, "mathematics": 66, "kiswahili": 75, "science": 69},
            {"term": "2-2025", "english": 73, "mathematics": 70, "kiswahili": 77, "science": 72},
        ]
    }
]



totals = {}

for student in students:
    total_score = 0

    for record in student["records"]:
        total_score += (
            record["english"] +
            record["mathematics"] +
            record["kiswahili"] +
            record["science"]
        )

    totals[student["student_id"]] = total_score



print("Total Scores Per Student:")
for student_id, total in totals.items():
    print(student_id, ":", total)
