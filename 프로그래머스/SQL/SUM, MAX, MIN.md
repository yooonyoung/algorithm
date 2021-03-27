1. 최댓값 구하기 https://programmers.co.kr/learn/courses/30/lessons/59415

   ```
   SELECT DATETIME FROM ANIMAL_INS ORDER BY DATETIME DESC LIMIT 1;
   ```

2. 최솟값 구하기 https://programmers.co.kr/learn/courses/30/lessons/59038

   ```
   SELECT DATETIME FROM ANIMAL_INS ORDER BY DATETIME LIMIT 1;
   ```

3. 동물 수 구하기 https://programmers.co.kr/learn/courses/30/lessons/59406

   ```
   SELECT COUNT(*) AS count FROM ANIMAL_INS;
   ```

4. 중복 제거하기 https://programmers.co.kr/learn/courses/30/lessons/59408

   ```
   SELECT COUNT(DISTINCT NAME) AS count FROM ANIMAL_INS;
   ```

   