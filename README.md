# work
class Freelancer:
    def __init__(self, name, skills, projects=[], overtime_hours=0):
        self.name = name
        self.skills = skills
        self.projects = projects
        self.overtime_hours = overtime_hours

    def add_project(self, project_name):
        self.projects.append(project_name)
        print(f"项目 '{project_name}' 已添加。")

    def record_overtime(self, hours):
        self.overtime_hours += hours
        print(f"已记录加班: {hours} 小时，总加班: {self.overtime_hours} 小时。")

    def show_profile(self):
        print(f"自由职业者姓名: {self.name}")
        print("技能: ", ', '.join(self.skills))
        print("已完成的项目: ", ', '.join(self.projects) if self.projects else "无")
        print(f"总加班时间: {self.overtime_hours} 小时")

    def calculate_income(self, hourly_rate, hours_worked):
        return hourly_rate * (hours_worked + self.overtime_hours)
