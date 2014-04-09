---
layout: post
title: "hello world"
date: 2014-04-08 22:35
comments: true
categories: [octopress]
---

**按照惯例，我的博客也应该以hello world开始。**

{% img bottom /images/blog/hello_world/helloworld.png %}

{% codeblock hello world lang:c %}
#ifdef __APPLE__
#include <GLUT/glut.h>          /* Open GL Util    APPLE */
#else
#include <GL/glut.h>            /* Open GL Util    OpenGL*/
#endif
#include <stdlib.h>

void drawCharactor(int ch) {
    float r = (float)rand()/RAND_MAX;
    float g = (float)rand()/RAND_MAX;
    float b = (float)rand()/RAND_MAX;
    glColor3f(r,g,b);
    glutStrokeCharacter(GLUT_STROKE_ROMAN, ch);
}

void displayCall() {
  glClear(GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT);
  glEnable(GL_DEPTH_TEST);

  glMatrixMode(GL_PROJECTION);
  glLoadIdentity();
  glOrtho(-2.0, 2.0, -2.0, 2.0, -2.0, 500.0);

  glMatrixMode(GL_MODELVIEW);
  glLoadIdentity();
  gluLookAt(2, 2, 2, 0.0, 0.0, 0.0, 0.0, 1.0, 0.0);
  glScalef(.005,.005,.005);
  glRotatef(20, 0, 1, 0);
  glRotatef(30, 0, 0, 1);
  glRotatef(5, 1, 0, 0);
  glTranslatef(-300, 0, 0);
    
  drawCharactor('H');
  drawCharactor('e');
  drawCharactor('l');
  drawCharactor('l');
  drawCharactor('o');
  
  drawCharactor('W');
  drawCharactor('o');
  drawCharactor('r');
  drawCharactor('l');
  drawCharactor('d');
  drawCharactor('!');
  
  glTranslatef(-400, -200, 0);
  drawCharactor('N');
  drawCharactor('e');
  drawCharactor('w');
  drawCharactor('e');
  drawCharactor('e');
  drawCharactor('r');
  glutSwapBuffers();
} /* end func displayCall */

/* Set up everything, and start the GLUT main loop. */
int main(int argc, char *argv[]) {
  glutInit(&argc, argv);
  glutInitDisplayMode(GLUT_RGB | GLUT_DOUBLE | GLUT_DEPTH);
  glutInitWindowSize(500, 500);
  glutInitWindowPosition(300, 200);
  glutCreateWindow("Hello World!");
  glutDisplayFunc(displayCall);
  glutMainLoop();
  return 0;
} /* end func main */
{% endcodeblock %}

