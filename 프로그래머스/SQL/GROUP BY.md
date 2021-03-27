1. 고양이와 개는 몇 마리 있을까 https://programmers.co.kr/learn/courses/30/lessons/59040

   ```
   SELECT ANIMAL_TYPE, COUNT(ANIMAL_TYPE) AS count FROM ANIMAL_INS GROUP BY ANIMAL_TYPE ORDER BY ANIMAL_TYPE;
   ```

2. 동명 동물 수 찾기 https://programmers.co.kr/learn/courses/30/lessons/59041

   ```
   SELECT NAME, COUNT(NAME) AS COUNT FROM ANIMAL_INS GROUP BY NAME HAVING COUNT >= 2 ORDER BY NAME;
   ```

3. 입양 시각 구하기(1) https://programmers.co.kr/learn/courses/30/lessons/59412

   ```
   SELECT HOUR(DATETIME) AS HOUR, COUNT(HOUR(DATETIME)) AS COUNT FROM ANIMAL_OUTS GROUP BY HOUR(DATETIME) HAVING HOUR BETWEEN 9 AND 20 ORDER BY HOUR(DATETIME);
   ```

4. 입양 시각 구하기(2)