#Analysis of an adolescent relationships network

@Mihaela Grigore (LeSc M1) //analysis produced as part of the Big Data course 2019 @CRI Paris https://github.com/Big-data-course-CRI/materials_big_data_cri_2019)
Content

    Introduction and motivation
    Choosing the dataset, overview of available dataset, loading data
    Numerical or analytical results
    Conclusions

Dataset description

    Dataset source: http://moreno.ss.uci.edu/data.html#adhealth

    The data contains information about friendships of students from communities with 1 or 2 highschool / junior highs. Details of datasets:
        - there are 84 communities in the dataset
        - each community has between 25 and 2587 students
        - relationship data: 'friendship' (from 0 to 15)
        - nodes attributes:
            - Sex is coded 1=male, 2=female, 0=unreported.
            - Race is coded 1=white, 2=black, 3=hispanic, 4=asian, 5=mixed/other, 0=unreported.
            - Grade is recorded as a number between 7 and 12 with 0=unreported.
            - And school codes are 0 and 1 when two schools were in a single community.

From the 84 community, we chose dataset from community 4 for this analysis. 

a. http://moreno.ss.uci.edu/comm4_att.dat - nodes attributes (291 students) DL
NR=457, NC=4

FORMAT = FULLMATRIX DIAGONAL PRESENT
COLUMN LABELS:
"sex"
"race"
"grade"
"school"
LEVEL LABELS:
"Page 1"
DATA:
2 3 10 1
2 1 10 1
1 1 10 1
....

b. http://moreno.ss.uci.edu/comm4.dat - relationships (1396 edges) DL
N=457
FORMAT=EDGELIST1
DATA:
1 123 4.00
1 127 2.00
1 128 3.00
....
Friendship information

Friendship has a score, therefore we are dealing with a weighted network. The relationship score is constructed as follows:

"For each friend named, the student was asked to check off whether he/she participated in any of five activities with the friend. These activities were:

    you went to (his/her) house in the last seven days.
    you met (him/her) after school to hang out or go somewhere in the last seven days.
    you spent time with (him/her) last weekend.
    you talked with (him/her) about a problem in the last seven days.
    you talked with (him/her) on the telephone in the last seven days.

These activities were summed to create a valued network. Ties range in value from 1, meaning the student nominated the friend but reported no activities, to 6, meaning the student nominated the friend and reported participating in all five activities with the friend."

//mind that the data was collected in 1994-1995, therefore the communication methods mentioned in the questions might seem a bit archaic to us now.

