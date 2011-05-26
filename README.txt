The OU Multi-response question type

This is a multiple-choice, multiple-response question type that was created by
Mahmound Kassaei and Tim Hunt at the Open University (http://www.open.ac.uk/).


This question type is compatible with Moodle 2.1+.

To install using git, type this command in the root of your Moodle install
    git clone git://github.com/timhunt/moodle-qtype_oumultiresponse.git question/type/oumultiresponse
Then add question/type/oumultiresponse to your git ignore.

Alternatively, download the zip from
    https://github.com/timhunt/moodle-qtype_oumultiresponse/zipball/master
unzip it into the question/type folder, and then rename the new folder to
oumultiresponse.


The main difference from the standard Moodle multiple choice question type is
in the way that grading works. When creating the question, the teacher just
indicates which choices are correct. If there are n correct choices, then the
student scores 1/n for each correct choice, and loses 1/n for each incorrect
choice. So for example, suppose the question is:

    Which of these animals are mammals?

    A. Dog
    B. Frog
    C. Toad
    D. Cat
    E. Cow
    F. Newt
    G. Lion

Then
    ADEG (4 right out of 4) scores 100%.
    D (1 right) scores 25%.
    ADEGF (4 right, 1 wrong) scores 75%.
    ADEBC (3 right, 2 wrong) scores 25%.

In interactive mode, the student is given more credit for choices that are
selected correctly on the first try, even if it takes more tries to get
some of the other choices correct.