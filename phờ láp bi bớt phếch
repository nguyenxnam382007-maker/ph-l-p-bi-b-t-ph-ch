import pygame
import sys
import random

# Khởi tạo Pygame
pygame.init()

SCREEN_WIDTH = 400
SCREEN_HEIGHT = 600
GRAVITY = 0.25
BIRD_MOVEMENT = 0
SCORE = 0
GAME_ACTIVE = True

screen = pygame.display.set_mode((SCREEN_WIDTH, SCREEN_HEIGHT))
clock = pygame.time.Clock()
font = pygame.font.SysFont("Arial", 32)

bird_rect = pygame.Rect(100, 300, 30, 30)

pipe_list = []
SPAWNPIPE = pygame.USEREVENT
pygame.time.set_timer(SPAWNPIPE, 1200) # Cứ 1.2s tạo 1 ống mới
pipe_height = [300, 400, 500]

def create_pipe():
    random_pipe_pos = random.choice(pipe_height)
    bottom_pipe = pygame.Rect(400, random_pipe_pos, 50, 600)
    top_pipe = pygame.Rect(400, random_pipe_pos - 750, 50, 600) # Khoảng trống là 150px
    return bottom_pipe, top_pipe

def move_pipes(pipes):
    for pipe in pipes:
        pipe.centerx -= 3
    return [pipe for pipe in
