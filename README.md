# PYTHON-PYGAME---SOLAR-ELLIPTICALS-
#SOLAR ELLIPTICALS 
#solar ellipticals 15
import pygame
import math
import sys


pygame.init()

screen = pygame.display.set_mode((600,300))
pygame.display.set_caption("ELLIPTICAL ORBIT")
clock = pygame.time.Clock()

while(True):
    for event in pygame .event.get():
      if event.type == pygame.QUIT:
          sys.exit()


    x_axis = 250
    y_axis = 100
    for degree in range(0,360,10):
       
       x1=int(math.cos(degree*2*math.pi/360)*x_axis) + 300
       y1=int(math.sin(degree*2*math.pi/360)*y_axis) +150
       screen.fill((0,0,0))
       pygame.draw.circle(screen,(255,0,0),[300,150],40)
       pygame.draw.ellipse(screen,(255,255,255),[50,50,500,200],1)
       pygame.draw.circle(screen,(0,255,0),[x1,y1],20)
       pygame.display.flip()
       clock.tick(5)
