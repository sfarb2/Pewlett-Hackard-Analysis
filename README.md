# Pewlett-Hackard-Analysis

## Overview of Project

### Purpose
The purpose of this project was to determine how many employees are retiring and how many existing employees are eligible to be mentored into replacement positions.

## Results

### Upcoming Retirements
As we can see from the image below, Pewlett-Hackard is about to get hit with an enormous wave of retirements.

![retirement_titles.png](/retirement_titles.png)

- More than 72,000 employees in total are eligible/expected to retire.

- The number of Senior Engineers and Senior Staff that will need to be replaced are both in the neighborhood of 25,000 - a staggering number of staffers reaching retirement!

### Available Mentors
Though this code block in Deliverable 2 shows the list of employees deemed eligible for mentorship:
```
SELECT DISTINCT ON (e.emp_no) e.emp_no, e.first_name, e.last_name, e.birth_date, ti.from_date, ti.to_date, ti.title
FROM employees e
JOIN dept_emp de ON e.emp_no = de.emp_no
JOIN titles ti ON e.emp_no = ti.emp_no
WHERE ti.to_date ='9999-01-01'
AND e.birth_date BETWEEN '1965-01-01' AND '1965-12-31'
ORDER BY e.emp_no;
```

It may be more useful to evaluate how many mentors are eligible/available by role:

![mentorship_eligibility.png](/mentorship_eligibility.png)

- The good news is that the roles that will suffer the most attrition also have the most eligible mentors (Senior Engineers and Senior Staff).

- The bad news is that each Senior Staff mentor would need to be accountable for nearly 44 new employees, and each Senior Engineer mentor would need to bring nearly 49 new staffers up to speed.

## Summary

### Recap of Staff Figures
As previously stated, more than 72,000 employees are slated/eligible to retire - a daunting number to replace. Pewlett-Hackard has approximately 1,500 team members ready to offer mentorship to new staffers; however, the load on each will be significant. Aside from Assistant Engineers, mentors at each tier of the organization will be responsible for coaching more than 40 replacements apiece (and there are no Managers eligible to become mentors at this time).

### Recommendation
In order to successfully weather this impending "silver tsunami", Pewlett-Hackard needs to focus on hiring immediately to ensure that it is able to replace the massive exodus of staff with new employees who have sufficient time to learn from a set of mentors who will be extremely taxed.
