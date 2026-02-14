import csv

students_dict = {}

with open("student score - Sheet1.csv", newline="") as file:
    reader = csv.DictReader(file)

    for row in reader:
        student_id = row["student_id"]


        english = int(row["english"])
        mathematics = int(row["mathematics"])
        kiswahili = int(row["kiswahili"])
        science = int(row["science"])

        term_total = english + mathematics + kiswahili + science

        record = {
            "term": row["term"],
            "english": english,
            "mathematics": mathematics,
            "kiswahili": kiswahili,
            "science": science,
            "term_total": term_total
        }

        if student_id not in students_dict:
            students_dict[student_id] = {
                "student_id": student_id,
                "records": []
            }

        students_dict[student_id]["records"].append(record)


students_list = list(students_dict.values())

totals = {}

for student in students_list:
    overall_total = 0

    for record in student["records"]:
        overall_total += record["term_total"]

    totals[student["student_id"]] = overall_total

print("Student Data:")
print(students_list)

print("Total Scores Per Student:")
for student_id, total in totals.items():
    print(student_id, ":", total)
