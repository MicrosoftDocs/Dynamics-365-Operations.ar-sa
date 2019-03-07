---
title: توزيع المستندات الواردة بتنسيق Excel
description: يوفر هذا الموضوع معلومات حول تصميم تنسيقات التقارير الإلكترونية لتحليل المعلومات التي تحتوي عليها ملفات Microsoft Excel الواردة.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 490a9325be25908564a40478a1ee29feea67fc02
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "367468"
---
# <a name="parse-incoming-documents-in-excel-format"></a><span data-ttu-id="84137-103">توزيع المستندات الواردة في تنسيق  Excel</span><span class="sxs-lookup"><span data-stu-id="84137-103">Parse incoming documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="84137-104">يمكنك تصميم تنسيقات التقارير الإلكترونية لتحليل ملفات Microsoft Excel الواردة التي تمثل البيانات في مصنفات Microsoft Excel (ملفات بتنسيق XLSX).</span><span class="sxs-lookup"><span data-stu-id="84137-104">You can design Electronic reporting (ER) formats to parse incoming Microsoft Excel files that represent data in Microsoft Excel workbooks (files in XLSX format).</span></span> <span data-ttu-id="84137-105">يمكنك بعد ذلك استخدام المحتوى من هذه الملفات لتحديث بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="84137-105">You can then use the content from these files to update application data.</span></span> <span data-ttu-id="84137-106">ويكون هذا مفيدًا في حالة:</span><span class="sxs-lookup"><span data-stu-id="84137-106">This is useful if you:</span></span>

- <span data-ttu-id="84137-107">تصميم نموذج جديد وتنسيق، واختبارهم في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="84137-107">Design a new model and format and want to test them at run-time.</span></span> <span data-ttu-id="84137-108">في هذه الحالة، سوف يقوم Excel بمحاكاة بيانات التطبيق الفعلية.</span><span class="sxs-lookup"><span data-stu-id="84137-108">In this case, Excel will simulate the actual application data.</span></span>
- <span data-ttu-id="84137-109">إدارة بيانات تتجاوز تطبيقك في Excel وتريد استيراد هذه البيانات لإرسال تقرير مُحدد.</span><span class="sxs-lookup"><span data-stu-id="84137-109">Manage data beyond your application in Excel and want to import this data to submit a specific report.</span></span>

<span data-ttu-id="84137-110">لمزيد من المعلومات حول هذه الميزة، قم بتشغيل دلائل المهام **التقارير الإلكترونية - استيراد بيانات من ملف Microsoft Excel (الجزء 1: تصميم التنسيق)** و**التقارير الإلكترونية - استيراد بيانات من ملف Microsoft Excel (الجزء 2: استيراد البيانات)** (أجزاء من عملية الأعمال 7.5.4.3 اكتساب/تطوير خدمة تكنولوجيا المعلومات/مكونات الحلول (10677)).</span><span class="sxs-lookup"><span data-stu-id="84137-110">To learn more about this feature, play the task guides **ER Import data from a Microsoft Excel file (Part 1: Design format)** and **ER Import data from a Microsoft Excel file (Part 2: Import data)** (parts of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span> <span data-ttu-id="84137-111">تتناول دلائل المهام هذه كيف يمكن نشر ملف Excel وارد باستخدام تنسيق ER لاستيراد معلومات من المستندات الواردة وتحديث بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="84137-111">These task guides walk through how the incoming Excel file can be parsed by using the ER format to import information from incoming documents and update application data.</span></span> <span data-ttu-id="84137-112">يمكنك تحميل ملفات دليل المهام من [مركز تحميل Microsoft](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="84137-112">You can download the task guide files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

<span data-ttu-id="84137-113">قم بتنزيل الملفات التالية لإكمال دلائل المهام المذكورة أعلاه.</span><span class="sxs-lookup"><span data-stu-id="84137-113">Download the following files to complete the task guides mentioned above.</span></span>

| <span data-ttu-id="84137-114">وصف المحتوى</span><span class="sxs-lookup"><span data-stu-id="84137-114">Content description</span></span>                         | <span data-ttu-id="84137-115">ملف</span><span class="sxs-lookup"><span data-stu-id="84137-115">File</span></span>                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="84137-116">ملف وارد بتنسيق XLSX- قالب</span><span class="sxs-lookup"><span data-stu-id="84137-116">Incoming file in .XLSX format - template</span></span>    | [<span data-ttu-id="84137-117">1099import-template.xlsx</span><span class="sxs-lookup"><span data-stu-id="84137-117">1099import-template.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |
| <span data-ttu-id="84137-118">ملف وارد بتنسيق XLSX- بيانات نموذجية</span><span class="sxs-lookup"><span data-stu-id="84137-118">Incoming file in .XLSX format - sample data</span></span> | [<span data-ttu-id="84137-119">1099import-data.xlsx</span><span class="sxs-lookup"><span data-stu-id="84137-119">1099import-data.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)     |

<span data-ttu-id="84137-120">إذا لم تقم بتشغيل دليل المهام التالي بعد، [‏‫التقارير الإلكترونية - إنشاء التكوينات المطلوبة لاستيراد البيانات من ملف خارجي‬](./tasks/er-required-configurations-import-data.md) في تطبيق Dynamics 365 for Finance and Operation الحالي، قم بتنزيل الملف التالي.</span><span class="sxs-lookup"><span data-stu-id="84137-120">If you have not yet played the following task guide, [ER Create required configurations to import data from an external file](./tasks/er-required-configurations-import-data.md) in the current Dynamics 365 for Finance and Operation application, download the following file.</span></span>

| <span data-ttu-id="84137-121">وصف المحتوى</span><span class="sxs-lookup"><span data-stu-id="84137-121">Content description</span></span>    | <span data-ttu-id="84137-122">ملف</span><span class="sxs-lookup"><span data-stu-id="84137-122">File</span></span>                                                            |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="84137-123">تكوين نموذج تقارير إلكترونية</span><span class="sxs-lookup"><span data-stu-id="84137-123">ER model configuration</span></span> | [<span data-ttu-id="84137-124">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="84137-124">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |
