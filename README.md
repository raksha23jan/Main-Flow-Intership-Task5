query 1: select 
    studentid,
    (MathScore + ScienceScore + EnglishScore)/3 AS total_score,
    CASE 
        WHEN (MathScore + ScienceScore + EnglishScore)/3 >= 90 THEN 'A'
        WHEN (MathScore + ScienceScore + EnglishScore)/3 >= 80 THEN 'B'
        WHEN (MathScore + ScienceScore + EnglishScore)/3 >= 70 THEN 'C'
        ELSE 'D (Fail)'
    END AS grade
FROM 
    student;

query 2: SELECT 
    studentid,
    MathScore,
    CASE 
        WHEN MathScore >= 40 THEN 'Pass' 
        ELSE 'Fail' 
    END AS Math_Status,
    ScienceScore,
    CASE 
        WHEN ScienceScore >= 40 THEN 'Pass' 
        ELSE 'Fail' 
    END AS Science_Status,
    EnglishScore,
    CASE 
        WHEN EnglishScore >= 40 THEN 'Pass' 
        ELSE 'Fail' 
    END AS English_Status

FROM 
    student;
