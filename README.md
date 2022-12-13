# Meuprimeirobancodedados
Meu primeiro banco de dados usando MySQL


CREATE DATABASE  IF NOT EXISTS `cadastro` /*!40100 DEFAULT CHARACTER SET utf8 */;
USE `cadastro`;
-- MySQL dump 10.13  Distrib 8.0.31, for Win64 (x86_64)
--
-- Host: localhost    Database: cadastro
-- ------------------------------------------------------
-- Server version	5.7.36

/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!50503 SET NAMES utf8 */;
/*!40103 SET @OLD_TIME_ZONE=@@TIME_ZONE */;
/*!40103 SET TIME_ZONE='+00:00' */;
/*!40014 SET @OLD_UNIQUE_CHECKS=@@UNIQUE_CHECKS, UNIQUE_CHECKS=0 */;
/*!40014 SET @OLD_FOREIGN_KEY_CHECKS=@@FOREIGN_KEY_CHECKS, FOREIGN_KEY_CHECKS=0 */;
/*!40101 SET @OLD_SQL_MODE=@@SQL_MODE, SQL_MODE='NO_AUTO_VALUE_ON_ZERO' */;
/*!40111 SET @OLD_SQL_NOTES=@@SQL_NOTES, SQL_NOTES=0 */;

--
-- Table structure for table `alunos`
--

DROP TABLE IF EXISTS `alunos`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `alunos` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `nome` varchar(30) NOT NULL,
  `profissao` varchar(10) DEFAULT NULL,
  `nascimento` date DEFAULT NULL,
  `sexo` enum('M','F') DEFAULT NULL,
  `peso` decimal(5,2) DEFAULT NULL,
  `altura` decimal(3,2) DEFAULT NULL,
  `nacionalidade` varchar(20) DEFAULT 'Brasil',
  PRIMARY KEY (`id`)
) ENGINE=MyISAM AUTO_INCREMENT=23 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `alunos`
--

LOCK TABLES `alunos` WRITE;
/*!40000 ALTER TABLE `alunos` DISABLE KEYS */;
INSERT INTO `alunos` VALUES (1,'Gisele',NULL,'1991-03-05','F',55.00,1.60,'Brasil'),(2,'Joana',NULL,'1985-12-03','F',55.00,1.70,'Colombia'),(3,'Maria',NULL,'1985-12-03','F',55.00,1.70,'Brasil'),(4,'Fernando',NULL,'1960-08-09','M',80.20,1.80,'Belgica'),(5,'Fernando',NULL,'1960-08-09','M',80.20,1.80,'Belgica'),(6,'Fernando',NULL,'1960-08-09','M',80.20,1.80,'Belgica'),(7,'Fernando',NULL,'1960-08-09','M',80.20,1.80,'Belgica'),(8,'Fernando',NULL,'1960-08-09','M',80.20,1.80,'Belgica'),(9,'Fernando',NULL,'1960-08-09','M',80.20,1.80,'Belgica'),(10,'Fernando',NULL,'1960-08-09','M',80.20,1.80,'Belgica'),(11,'Fernando',NULL,'1960-08-09','M',80.20,1.80,'Belgica'),(12,'Fernando',NULL,'1960-08-09','M',80.20,1.80,'Belgica'),(13,'Fernando',NULL,'1960-08-09','M',80.20,1.80,'Belgica'),(14,'Murilo',NULL,'1999-07-27','M',76.00,1.77,'Brasil'),(15,'Fernando',NULL,'1960-08-09','M',80.20,1.80,'Belgica'),(16,'Murilo',NULL,'1999-07-27','M',76.00,1.77,'Brasil'),(17,'Fernando',NULL,'1960-08-09','M',80.20,1.80,'Belgica'),(18,'Murilo',NULL,'1999-07-27','M',76.00,1.77,'Brasil'),(19,'Juliana',NULL,'1995-12-28','F',58.00,1.69,'Noruega'),(20,'Fernando',NULL,'1960-08-09','M',80.20,1.80,'Belgica'),(21,'Igor',NULL,'1988-11-27','M',76.00,1.77,'Brasil'),(22,'Juliana',NULL,'1995-12-28','F',58.00,1.69,'Noruega');
/*!40000 ALTER TABLE `alunos` ENABLE KEYS */;
UNLOCK TABLES;
/*!40103 SET TIME_ZONE=@OLD_TIME_ZONE */;

/*!40101 SET SQL_MODE=@OLD_SQL_MODE */;
/*!40014 SET FOREIGN_KEY_CHECKS=@OLD_FOREIGN_KEY_CHECKS */;
/*!40014 SET UNIQUE_CHECKS=@OLD_UNIQUE_CHECKS */;
/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
/*!40111 SET SQL_NOTES=@OLD_SQL_NOTES */;

-- Dump completed on 2022-12-13 19:32:01



CREATE DATABASE  IF NOT EXISTS `cadastro` /*!40100 DEFAULT CHARACTER SET utf8 */;
USE `cadastro`;
-- MySQL dump 10.13  Distrib 8.0.31, for Win64 (x86_64)
--
-- Host: localhost    Database: cadastro
-- ------------------------------------------------------
-- Server version	5.7.36

/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!50503 SET NAMES utf8 */;
/*!40103 SET @OLD_TIME_ZONE=@@TIME_ZONE */;
/*!40103 SET TIME_ZONE='+00:00' */;
/*!40014 SET @OLD_UNIQUE_CHECKS=@@UNIQUE_CHECKS, UNIQUE_CHECKS=0 */;
/*!40014 SET @OLD_FOREIGN_KEY_CHECKS=@@FOREIGN_KEY_CHECKS, FOREIGN_KEY_CHECKS=0 */;
/*!40101 SET @OLD_SQL_MODE=@@SQL_MODE, SQL_MODE='NO_AUTO_VALUE_ON_ZERO' */;
/*!40111 SET @OLD_SQL_NOTES=@@SQL_NOTES, SQL_NOTES=0 */;

--
-- Table structure for table `cursos`
--

DROP TABLE IF EXISTS `cursos`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `cursos` (
  `idcurso` int(11) NOT NULL,
  `Nome` varchar(30) NOT NULL,
  `Descriçao` text,
  `Carga` int(10) unsigned DEFAULT NULL,
  `Totaulas` int(10) unsigned DEFAULT NULL,
  `Ano` year(4) DEFAULT '2022',
  PRIMARY KEY (`idcurso`),
  UNIQUE KEY `Nome` (`Nome`)
) ENGINE=MyISAM DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `cursos`
--

LOCK TABLES `cursos` WRITE;
/*!40000 ALTER TABLE `cursos` DISABLE KEYS */;
INSERT INTO `cursos` VALUES (1,'HTML5','Cursos de HTML5',40,37,2022),(2,'Algoritmos','Logica de programação',20,15,2022),(3,'Photoshop','Dicas de photoshop CC',10,8,2022),(4,'PHP','Cursos de PHP para iniciantes',40,20,2015),(5,'Java','Introdução a linguagem Java',10,29,2019),(6,'MYSQL','Banco de dados MYSQL',30,15,2017),(7,'Word','Curso completo de Word',40,30,2016),(9,'Excel','Aprenda a fazer uma planilha',40,30,2009),(10,'PowerBI','Criando um Dashboard',5,2,2022);
/*!40000 ALTER TABLE `cursos` ENABLE KEYS */;
UNLOCK TABLES;
/*!40103 SET TIME_ZONE=@OLD_TIME_ZONE */;

/*!40101 SET SQL_MODE=@OLD_SQL_MODE */;
/*!40014 SET FOREIGN_KEY_CHECKS=@OLD_FOREIGN_KEY_CHECKS */;
/*!40014 SET UNIQUE_CHECKS=@OLD_UNIQUE_CHECKS */;
/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
/*!40111 SET SQL_NOTES=@OLD_SQL_NOTES */;

-- Dump completed on 2022-12-13 19:32:01
