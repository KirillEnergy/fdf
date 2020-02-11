# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: lrosalee <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2019/04/11 19:57:51 by lrosalee          #+#    #+#              #
#    Updated: 2020/02/10 20:04:42 by lrosalee         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

# NAME = libft.a
# CC = gcc
# INCLUDES = -I$(HEAD_DIR)
# HEAD_LIST = libft.h \
# 	get_next_line.h
# HEAD_DIR = ./includes/
# HEADERS = $(addprefix $(HEAD_DIR), $(HEAD_LIST))
# SRC_DIR = ./sources/
# SRC_LIST = ft_atoi.c \

NAME = libft.a
CC = gcc
FLAGS = -Wall -Werror -Wextra -O3 -c
INCLUDES = -I$(HEADERS_DIRECTORY)
HEADERS_LIST = libft.h\
	get_next_line.h
HEADERS_DIRECTORY = ./includes/
HEADERS = $(addprefix $(HEADERS_DIRECTORY), $(HEADERS_LIST))
SOURCES_DIRECTORY = ./sources/
SOURCES_LIST = 	ft_atoi.c \
	ft_memset.c\
	ft_atoi_base.c \
	ft_strlen.c \
	ft_strcmp.c \
	ft_strncmp.c \
	ft_strstr.c \
	ft_strnstr.c \
	ft_memset.c \
	ft_bzero.c \
	ft_memcpy.c \
	ft_memccpy.c \
	ft_memmove.c \
	ft_memchr.c \
	ft_memcmp.c \
	ft_strdup.c \
	ft_strndup.c \
	ft_strcpy.c \
	ft_strncpy.c \
	ft_strcat.c \
	ft_strncat.c \
	ft_strlcat.c \
	ft_strchr.c \
	ft_strrchr.c \
	ft_isalpha.c \
	ft_isdigit.c \
	ft_isalnum.c \
	ft_isascii.c \
	ft_isprint.c \
	ft_toupper.c \
	ft_tolower.c \
	ft_memalloc.c \
	ft_memdel.c \
	ft_strnew.c \
	ft_strdel.c \
	ft_strclr.c \
	ft_striter.c \
	ft_striteri.c \
	ft_strmap.c \
	ft_strmapi.c \
	ft_strequ.c \
	ft_strnequ.c \
	ft_strsub.c \
	ft_strjoin.c \
	ft_strtrim.c \
	ft_putchar.c \
	ft_putchar_fd.c \
	ft_strsplit.c \
	ft_itoa.c \
	ft_putstr.c \
	ft_putstr_fd.c \
	ft_putendl_fd.c \
	ft_putendl.c \
	ft_putnbr.c \
	ft_putnbr_fd.c \
	ft_abs.c \
	ft_min.c \
	ft_pow.c \
	ft_fact.c \
	ft_sqrt.c \
	ft_lstnew.c \
	ft_lstdelone.c \
	ft_lstdel.c \
	ft_lstadd.c \
	ft_lstiter.c \
	ft_lstmap.c \
	ft_realloc.c \
	get_next_line.c
# SRC = $(addprefix $(SRC_DIR), $(SRC_LIST))
# OBJ_DIR = objects/
# OBJ_LIST = $(patsubst %.c, %.o, $(SRC_LIST))
# OBJ = $(addprefix $(OBJ_DIR), $(OBJ_LIST))

# RM = rm -f
# CFLAGS = -Wall -Wextra -Werror

# all: $(NAME)

# $(NAME): $(OBJ_DIR) $(OBJ)
# 	gcc $(CFLAGS) -c $(SRC_LIST) 
# 	ar rc $(NAME) $(OBJ)
# 	ranlib $(NAME)

# $(OBJ_DIR):
# 	@mkdir -p $(OBJ_DIR)

# $(OBJ_DIR)%.o : $(SRC_DIR)%.c $(HEADERS)
# 	@$(CC) $(CFLAGS) $(INCLUDES) $< -o $@

# clean:
# 	@rm -rf $(OBJ_DIR)

# fclean: clean
# 	$(RM) $(NAME)

# re: fclean all

SOURCES = $(addprefix $(SOURCES_DIRECTORY), $(SOURCES_LIST))
OBJECTS_DIRECTORY = objects/
OBJECTS_LIST = $(patsubst %.c, %.o, $(SOURCES_LIST))
OBJECTS	= $(addprefix $(OBJECTS_DIRECTORY), $(OBJECTS_LIST))

# COLORS

GREEN = \033[0;32m
RED = \033[0;31m
RESET = \033[0m

.PHONY: all clean fclean re

all: $(NAME)

$(NAME): $(OBJECTS_DIRECTORY) $(OBJECTS)
	@ar rc $(NAME) $(OBJECTS)
	@ranlib $(NAME)
	@echo "\n$(NAME): $(GREEN)object files were created$(RESET)"
	@echo "$(NAME): $(GREEN)$(NAME) was created$(RESET)"

$(OBJECTS_DIRECTORY):
	@mkdir -p $(OBJECTS_DIRECTORY)
	@echo "$(NAME): $(GREEN)$(OBJECTS_DIRECTORY) was created$(RESET)"

$(OBJECTS_DIRECTORY)%.o : $(SOURCES_DIRECTORY)%.c $(HEADERS)
	@$(CC) $(FLAGS) $(INCLUDES) $< -o $@
	@echo "$(GREEN).$(RESET)\c"

clean:
	@rm -rf $(OBJECTS_DIRECTORY)
	@echo "$(NAME): $(RED)$(OBJECTS_DIRECTORY) was deleted$(RESET)"
	@echo "$(NAME): $(RED)object files were deleted$(RESET)"

fclean: clean
	@rm -f $(NAME)
	@echo "$(NAME): $(RED)$(NAME) was deleted$(RESET)"

re:
	@$(MAKE) fclean
	@$(MAKE) all