
.. _Set up Discussions in Cohorted Courses:


######################################################
Setting up Discussions in Courses with Student Cohorts
######################################################

By using cohort groups in a course and creating discussion topics that are
divided by cohort, you provide students with the ability to ask questions of,
and have conversations with, other members of their cohort. Cohort-only
discussion opportunities can help students develop a sense of community, provide
specialized experiences, and encourage deeper, more meaningful course
involvement.

When you first enable cohorts in your course, all course-wide discussion topics
provide unified access to posts for all students. You can configure one or more
of the course-wide topics to be divided by cohort instead. For details, see :ref:`Configure CourseWide Discussion Topics as Private`.

.. note:: The content-specific discussion topics in the course, which are 
 added to units as discussion components, are always divided by cohort.

For overview information about discussions in a course, see :ref:`Discussions`.
For information about using cohort groups in a course, see :ref:`Cohorts
Overview` and :ref:`Enabling and Configuring Cohorts`.


**************************************************
Course-Wide Discussion Topics Are Configurable
**************************************************

To create course-wide discussion topics, you add them on the **Advanced
Settings** page in Studio. By default, each of these topics is unified. All of
the students in the course can post, read, respond, and comment in course-wide
discussion topics without regard to their cohort group assignments. After you
add a course-wide topic, you can configure it so that it is divided by cohort
instead.

For example, in addition to the General topic, which is supplied by default,
you create these additional course-wide topics: Course Q&A, Announcements, and
Brainstorming. You want all students to be able to read and contribute to all
of the posts in the General and Course Q&A topics. However, you want the
Announcements and Brainstorming topics to be divided, so that students will
only be able to read and respond to contributions by the members of their own
cohorts. You complete the additional configuration step for the Announcements
and Brainstorming topics only.

For information about course-wide discussion topics, see
:ref:`Organizing_discussions`. For information about configuring these topics, 
see :ref:`Configure CourseWide Discussion Topics as Private`.


**************************************************
All Content-Specific Discussion Topics Are Divided
**************************************************

Each of the content-specific discussion topics is divided by cohort. A student
who is assigned to one cohort group cannot read or add to the posts, responses,
or comments contributed by the members of another cohort group.

To create content-specific discussion topics in a course, you add units that
include discussion components. In a course with the cohort feature enabled, you
do not have the option to change these topics to be unified for all students.

For more information about content-specific discussion topics,
see :ref:`Organizing_discussions`.


******************************************
Course-Wide Discussion Topics and Cohorts
******************************************

When you first :ref:`create a course-wide discussion topic<Create CourseWide
Discussion Topics>`, it is unified, and all students in the course can post,
read, respond, and comment in the topic without regard to their cohort group
assignments. After you add a course-wide topic, you can configure it so that it
is divided by cohort instead.


.. _Identifying Private CourseWide Discussion Topics:

=============================================================
Example: Configuring Course-Wide Discussion Topics As Divided
=============================================================

This example assumes that you have added three course-wide discussion topics
called Course Q&A, Announcements, and Brainstorming, to your course, so that in
addition to the system-supplied General topic, you have four course-wide
discussion topics. 

.. image:: ../Images/Discussion_Add_cohort_topics.png
 :alt: Discussion Topic Mapping field with four course-wide discussion topics 
       defined

You have now enabled cohorts for your course and would like
to take advantage of that feature as it applies to discussion topics.

The posts that you intend to make to the Course Q&A and General topics, and the
subjects you expect students to explore there, are appropriate for a unified
student audience. However, you also want to give students some course-wide
topics that are divided by cohort. You decide that the Announcements and
Brainstorming course-wide topics should be divided by cohort.

You also decide to apply a naming convention so that students will know the
audience for the discussion topics before they add any posts. For information on
how to achieve this, see :ref:`Apply Naming Conventions to Discussion Topics`.


.. _Configure CourseWide Discussion Topics as Private:

======================================================
Configure Course-Wide Discussion Topics as Divided
======================================================

This procedure shows how to configure the Brainstorming and Announcements
course-wide discussion topics (from the example in :ref:`Identifying Private
CourseWide Discussion Topics`) so that they are divided by cohort.

On the Studio **Advanced Settings** page, details of the two topics appear as
follows in the **Discussion Topic Mapping** field. You use the ID for each
discussion topic to identify it in the steps that follow.

.. code::

      "Brainstorming (private)": {
          "id": "i4x-edX-Open-edx_demo_course_brainstorming"
      },
      "Announcements (private)": {
          "id": "i4x-edX-Open-edx_demo_course_announcements"
      }

#. Open the course in Studio. 

#. Select **Settings**, then **Advanced Settings**.

#. In the **Cohort Configuration** field, place your cursor after the opening
   brace character (``{``) and press **Enter**.

#. On the new line, you define the ``"cohorted_discussions":`` policy key,
   followed by one or more course-wide discussion topic IDs enclosed by    square
   brackets (``[ ]``). You can define just one discussion topic or a set of
   discussion topics.

   For example, to define a single discussion topic, type
   ``"cohorted_discussions": ["discussion-topic-ID"]``, replacing "discussion-
   topic-ID" with your discussion topic's ID, and then press Enter.

   To define a set of topics, type the value of the "id" for each discussion
   topic on a new line, enclose it within quotation marks (``" "``), and
   separate the quoted "id" values with commas. For example:

 .. code:: 

   "cohorted_discussions": [
       "i4x-edX-Open-edx_demo_course_announcements",
       "i4x-edX-Open-edx_demo_course_brainstorming"
   ]
   
5. If "cohorted_discussions" is followed by other policy keys within the
   **Cohort Configuration** field, make sure there is a comma after the closing
   square bracket character (``],``). You must include a comma to separate each of
   the policy keys that you define.

.. Adding a line to force a line space

6. Click **Save Changes**. Studio resequences and reformats your entry.

 .. image:: ../Images/Configure_cohort_topic.png
  :alt: Cohort Configuration dictionary field with the cohorted_discussions key
        defined

7. Scroll back to the **Cohort Configuration** field to verify that your entry
   was saved as you expect. Entries that do not contain all of the required
   punctuation characters revert to the previous value when you save, and no
   warning is presented.

