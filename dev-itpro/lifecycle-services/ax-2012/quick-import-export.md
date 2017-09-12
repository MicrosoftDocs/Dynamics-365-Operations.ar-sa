---
title: "استخدام ميزة الاستيراد/التصدير السريع"
description: "الغرض من ميزة الاستيراد والتصدير السريع هو السماح لك بالاستيراد والتصدير من خلال تنفيذ عدد أقل من الخطوات."
author: margoc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: ax-2012
audience: Application User
ms.reviewer: margoc
ms.search.scope: AX 2012 R3 CU8, UnifiedOperations
ms.custom: 89041
ms.assetid: 990d64e6-d436-4c79-9bb5-bf8c5c5a048f
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 
ms.dyn365.ops.version: AX 2012 R3 CU8
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 121d8f757e2d5453308d8846bd299f3db339db67
ms.contentlocale: ar-sa
ms.lasthandoff: 07/18/2017

---

# <a name="run-the-test-data-transfer-tool-beta-for-dynamics-ax-ax-2012"></a><span data-ttu-id="81553-103">تشغيل ‏‫أداة تحويل بيانات الاختبار (بيتا) لـ Dynamics AX ‏(AX 2012)</span><span class="sxs-lookup"><span data-stu-id="81553-103">Run the Test Data Transfer Tool (beta) for Dynamics AX (AX 2012)</span></span>

[!include[banner](../../includes/banner.md)]


<span data-ttu-id="81553-104">الغرض من ميزة الاستيراد والتصدير السريع هو السماح لك بالاستيراد والتصدير من خلال تنفيذ عدد أقل من الخطوات.</span><span class="sxs-lookup"><span data-stu-id="81553-104">The purpose of Quick import export is to let you import and export with fewer steps.</span></span>

<span data-ttu-id="81553-105">لقد أضفنا ميزة "الاستيراد والتصدير السريع" للسماح للمستخدمين باستيراد أو تصدير مهام بسيطة يرغبون في تنفيذها بسرعة.</span><span class="sxs-lookup"><span data-stu-id="81553-105">We added the Quick Import Export feature to let users import or export simple jobs that they want to execute quickly.</span></span> <span data-ttu-id="81553-106">يتم استخدام هذه الميزة بشكل مثالي في السيناريوهات حيث يتم تعيين ملف بشكل تلقائي إلى النظام، ولا يحتاج المستخدم إلى التنقل عبر التعيينات المتقدمة أو إنشاء مهام استيراد أو تصدير متكررة.</span><span class="sxs-lookup"><span data-stu-id="81553-106">Ideally this feature is used in scenarios in which a file automatically maps to the system and user does not need to go through advanced mapping or create repeated import or export jobs.</span></span>

-   <span data-ttu-id="81553-107">تدعم هذه الميزة العمل مع الكيانات الجاهزة والكيانات المخصصة على حدٍ سواء.</span><span class="sxs-lookup"><span data-stu-id="81553-107">This feature supports working with both out-of-the-box and custom entities.</span></span>
-   <span data-ttu-id="81553-108">يمكنك الاستيراد من الملفات، وإذا كنت تستخدم مصدر بيانات ODBC، فيمكنك تحديد استعلام لاستخدامه لتعريف الاستيراد.</span><span class="sxs-lookup"><span data-stu-id="81553-108">You can import from files, and if you are using an ODBC data source, you can select a query to use to define your import.</span></span>
-   <span data-ttu-id="81553-109">يجب أن تقوم مسبقًا بتعريف تنسيقات البيانات المصدر إما لتطبيق AX أو للملف، كما يجب عليك معرفة موقعها.</span><span class="sxs-lookup"><span data-stu-id="81553-109">You must have previously defined source data formats for either AX or File, and know where they are located.</span></span>
-   <span data-ttu-id="81553-110">لا تحتاج إلى إنشاء مجموعة معالجة لاستخدام الاستيراد/التصدير السريع، إذ سيتم إنشاء هذه المجموعة تلقائيًا بواسطة النظام عند تنفيذ مهمة الاستيراد أو التصدير.</span><span class="sxs-lookup"><span data-stu-id="81553-110">You do not need to create a processing group to use quick import/export, one will be automatically created by the system when executing the import or export job.</span></span> <span data-ttu-id="81553-111">يمكنك أيضًا السماح باستيراد محفوظات البيانات بواسطة ميزة الاستيراد/التصدير السريع.</span><span class="sxs-lookup"><span data-stu-id="81553-111">You can also choose keep the history of the data imported by the quick import/export.</span></span>

  <span data-ttu-id="81553-112">تجدر الإشارة إلى أن ميزة الاستيراد والتصدير السريع تفترض بأنك على دراية بمفاهيم DIXF.</span><span class="sxs-lookup"><span data-stu-id="81553-112">Note that Quick import export assumes that you are familiar with the concepts of DIXF.</span></span>




