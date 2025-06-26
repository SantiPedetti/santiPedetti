### Hi there 👋

BEGIN TRANSACTION;

INSERT INTO master.dbo.Users (Name,LastName,Email,BirthDate,Password,SystemAdmin,ProjectAdmin,ProjectLeader) VALUES
	 (N'Camila',N'apellido',N'Camila@gmail.com','2000-01-20 00:00:00.0000000',N'IBi6HrrTcJvhrQ/pEHH0saJEWqcaMwwcD46KPRtynlI=',0,1,0),
	 (N'Sofia',N'Apellido',N'sofia@gmail.com','2000-10-10 00:00:00.0000000',N'v3OO4QtaBeefa8lRX+S7H5QlIc+vRy9NeBpJJE/dOzE=',0,0,1),
	 (N'Pilar',N'Apellido',N'pilar@gmail.com','2000-12-12 00:00:00.0000000',N'nPcquWemVeU9xKIen2OLvCFe7L6utNk3DZNVcpHFAr8=',0,0,0),
	 (N'Maia',N'apellido',N'maia@gmail.com','1999-12-12 00:00:00.0000000',N'wqpYI3Y6N3+XKIggeVP5dNtwIYn1gwDZ2mYME5FLh5o=',0,0,0),
	 (N'Santiago',N'apellido',N'santi@gmail.com','2001-02-22 00:00:00.0000000',N'cAj5gn5Hdb2JbyBK83s6XtWzHdmkLNWhU5W8XQgySW4=',0,0,0),
	 (N'Juan',N'apellido',N'juan@gmail.com','2003-06-26 00:00:00.0000000',N'NhyFoVwMoMd3D6nVNXH2gDqgcOXdVgcgL2tAAMWo64g=',0,0,1),
	 (N'Jose',N'apellido',N'jose@gmail.com','2004-11-11 00:00:00.0000000',N'wDoQhEfV9RNgnCsI95pAq/G4XwPz1gRi8CvuJTvK26I=',0,0,1),
	 (N'Pedro',N'apellido',N'pedro@gmail.com','2001-09-29 00:00:00.0000000',N'4SFWNm2mTLNbFQO59OhfFMdd4iQezexdyvD6hDW/2tE=',0,0,0),
	 (N'Clara',N'apellido',N'clara@gmail.com','2002-09-09 00:00:00.0000000',N'Li3mVKHKhXW4klcZfzFVJQT/BYnJ1lNEC/wTo50myeo=',0,0,0);

INSERT INTO master.dbo.Users (Name,LastName,Email,BirthDate,Password,SystemAdmin,ProjectAdmin,ProjectLeader) VALUES
	 (N'Celeste',N'apellido',N'celeste@gmail.com','2003-02-22 00:00:00.0000000',N'8GxlQuT1M+EvceEGsdheBThCuF1iP3r1X/rz+G9t+UI=',0,0,0);

INSERT INTO master.dbo.Projects (Name,Description,StartDate,AdminId,LeaderId) VALUES
	 (N'Proyecto1',N'----','2025-06-25 00:00:00.0000000',2,3),
	 (N'Proyecto2',N'-----','2025-06-25 00:00:00.0000000',2,3),
	 (N'Proyecto3',N'----','2025-06-25 00:00:00.0000000',2,3),
	 (N'Proyecto4',N'-----','2025-06-25 00:00:00.0000000',2,7),
	 (N'Proyecto5',N'------','2025-06-25 00:00:00.0000000',2,7),
	 (N'Proyecto6',N'----','2025-06-25 00:00:00.0000000',2,7),
	 (N'Proyecto7',N'------','2025-06-25 00:00:00.0000000',2,8),
	 (N'Proyecto8',N'-------','2025-06-25 00:00:00.0000000',2,8),
	 (N'Proyecto9',N'----','2025-06-25 00:00:00.0000000',2,8),
	 (N'Proyecto10',N'----','2025-06-25 00:00:00.0000000',2,8);

INSERT INTO master.dbo.Resources (Name,[Type],Description,Quantity,ProjectId) VALUES
	 (N'RECURSO1',N'TIPO1',N'------',2,NULL),
	 (N'RECURSO2',N'TIPO2',N'-------',1,NULL),
	 (N'RECURSO3',N'TIPO2',N'----',2,NULL),
	 (N'RECURSO4',N'TIPO4',N'---',1,NULL),
	 (N'RECURSO5',N'TIPO5',N'---',1,NULL),
	 (N'RECURSO6',N'TIPO6',N'---',1,NULL),
	 (N'RECURSO1',N'TIPO1',N'----',1,NULL),
	 (N'RECURSO1',N'TIPO1',N'--------',2,1),
	 (N'RECURSO2',N'TIPO2',N'-----',2,1),
	 (N'RECURSO3',N'TIPO2',N'------',0,1);

INSERT INTO master.dbo.Resources (Name,[Type],Description,Quantity,ProjectId) VALUES
	 (N'RECURSO4',N'TIPO4',N'----',1,10),
	 (N'RECURSO5',N'TIPO5',N'---',1,10),
	 (N'RECURSO6',N'TIPO6',N'----',2,10);

INSERT INTO master.dbo.ProjectTasks (ProjectName,Finished,Title,Description,StartDate,Duration,ProjectId,UserId,IsAssigned) VALUES
	 (N'Proyecto1',0,N'T1',N'-------','2025-06-25 00:00:00.0000000',3,1,4,1),
	 (N'Proyecto2',0,N'T2',N'----------','2025-06-26 00:00:00.0000000',4,2,5,1),
	 (N'Proyecto3',0,N'T3',N'-----','2025-06-30 00:00:00.0000000',3,3,6,1),
	 (N'Proyecto4',0,N'T4',N'-----','2025-06-30 00:00:00.0000000',2,4,11,1),
	 (N'Proyecto5',0,N'T5',N'-----','2025-06-27 00:00:00.0000000',6,5,10,1),
	 (N'Proyecto6',0,N'T6',N'------','2025-06-25 00:00:00.0000000',9,6,9,1),
	 (N'Proyecto7',0,N'T7',N'-----','2025-06-28 00:00:00.0000000',4,7,7,1),
	 (N'Proyecto8',0,N'T8',N'-------','2025-06-30 00:00:00.0000000',6,8,8,1),
	 (N'Proyecto5',0,N'T9',N'-------','2025-06-30 00:00:00.0000000',2,5,10,1),
	 (N'Proyecto9',0,N'T10',N'-----','2025-06-25 00:00:00.0000000',5,9,2,1);

INSERT INTO master.dbo.ProjectTasks (ProjectName,Finished,Title,Description,StartDate,Duration,ProjectId,UserId,IsAssigned) VALUES
	 (N'Proyecto1',0,N'T11',N'-----','2025-06-26 00:00:00.0000000',4,1,4,1),
	 (N'Proyecto1',0,N'T12',N'-----','2025-06-26 00:00:00.0000000',5,1,4,1),
	 (N'Proyecto2',0,N'T13',N'------','2025-06-27 00:00:00.0000000',5,2,5,1),
	 (N'Proyecto2',0,N'T14',N'----------','2025-06-29 00:00:00.0000000',4,2,5,1),
	 (N'Proyecto3',0,N'T15',N'------','2025-06-25 00:00:00.0000000',3,3,6,1),
	 (N'Proyecto3',0,N'T16',N'------','2025-06-28 00:00:00.0000000',7,3,6,1),
	 (N'Proyecto4',0,N'T17',N'-------','2025-07-01 00:00:00.0000000',2,4,11,1),
	 (N'Proyecto4',0,N'T18',N'-----','2025-06-25 00:00:00.0000000',5,4,11,1),
	 (N'Proyecto10',0,N'T19',N'-----','2025-06-25 00:00:00.0000000',5,10,1,1),
	 (N'Proyecto5',0,N'T20',N'------','2025-06-25 00:00:00.0000000',4,5,10,1);

INSERT INTO master.dbo.ProjectTasks (ProjectName,Finished,Title,Description,StartDate,Duration,ProjectId,UserId,IsAssigned) VALUES
	 (N'Proyecto1',0,N'T21',N'-----','2025-06-26 00:00:00.0000000',5,1,4,1);

INSERT INTO master.dbo.ProjectUsers (ProjectId,UsersId) VALUES
	 (10,1),
	 (1,2),
	 (2,2),
	 (3,2),
	 (4,2),
	 (5,2),
	 (6,2),
	 (7,2),
	 (8,2),
	 (9,2);

INSERT INTO master.dbo.ProjectUsers (ProjectId,UsersId) VALUES
	 (10,2),
	 (1,3),
	 (2,3),
	 (3,3),
	 (1,4),
	 (2,5),
	 (3,6),
	 (4,7),
	 (5,7),
	 (6,7);

INSERT INTO master.dbo.ProjectUsers (ProjectId,UsersId) VALUES
	 (7,7),
	 (7,8),
	 (8,8),
	 (9,8),
	 (10,8),
	 (6,9),
	 (5,10),
	 (4,11);

INSERT INTO master.dbo.ProjectTaskResources (NecessaryResourcesId,ProjectTasksId) VALUES
	 (1,1),
	 (2,11),
	 (3,12),
	 (4,19),
	 (5,19),
	 (6,19),
	 (7,21);

INSERT INTO master.dbo.ProjectTaskProjectTask (DependenciesId,ProjectTaskId) VALUES
	 (5,9),
	 (1,11),
	 (1,12),
	 (2,13),
	 (2,14),
	 (3,15),
	 (3,16),
	 (4,17),
	 (4,18),
	 (5,20);

INSERT INTO master.dbo.Notifications (Message,CreatedAt,UserId) VALUES
	 (N'The project: Proyecto8 has been edited, the new Early finish is: 01/07/2025','2025-06-25 21:32:28.6900220',2),
	 (N'The project: Proyecto8 has been edited, the new Early finish is: 01/07/2025','2025-06-25 21:32:28.6905965',8);

COMMIT;
