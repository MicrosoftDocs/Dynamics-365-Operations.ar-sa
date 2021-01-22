---
title: ‏‫تشخيصات الأمان‬ لتسجيلات المهام
description: يوفر هذا الموضوع معلومات حول كيفيه تحليل متطلبات أذونات الأمان وإدارتها استنادا إلى تسجيل مهمة.
author: Peakerbl
manager: AnnBe
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.openlocfilehash: 4aecda7e0d604b70dec58a4f5bb2992fe7e0a5e2
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982420"
---
# <a name="security-diagnostics-for-task-recordings"></a><span data-ttu-id="995a0-103">‏‫تشخيصات الأمان‬ لتسجيلات المهام</span><span class="sxs-lookup"><span data-stu-id="995a0-103">Security diagnostics for task recordings</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a><span data-ttu-id="995a0-104">قبل البدء</span><span class="sxs-lookup"><span data-stu-id="995a0-104">Before you begin</span></span>

<span data-ttu-id="995a0-105">يوفر هذا الموضوع معلومات حول كيفيه تحليل متطلبات أذونات الأمان وإدارتها استنادا إلى تسجيل مهمة.</span><span class="sxs-lookup"><span data-stu-id="995a0-105">This topic provides information about how to analyze and manage security permission requirements based on a task recording.</span></span> <span data-ttu-id="995a0-106">قبل إكمال الخطوات الواردة في هذا الموضوع، يجب أن يكون لديك تسجيل مهمة للعملية التجارية التي ترغب في تحليلها.</span><span class="sxs-lookup"><span data-stu-id="995a0-106">Before you complete the steps in this topic, you must have a task recording of the business process that you want to analyze.</span></span> <span data-ttu-id="995a0-107">لتسجيل عمليه تجاريه، راجع [موارد مسجل المهام‬‏‫](../../user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="995a0-107">To record a business process, see [Task recorder resources](../../user-interface/task-recorder.md).</span></span> 

## <a name="manage-security-for-a-task-recording"></a><span data-ttu-id="995a0-108">إدارة الأمان لتسجيل مهمة</span><span class="sxs-lookup"><span data-stu-id="995a0-108">Manage security for a task recording</span></span>

1. <span data-ttu-id="995a0-109">انتقل إلى **إدارة النظام** > **الأمان** > **تشخيص الأمان لتسجيل المهام** .</span><span class="sxs-lookup"><span data-stu-id="995a0-109">Go to **System administration** > **Security** > **Security diagnostic for task recording** .</span></span>
2. <span data-ttu-id="995a0-110">افتح تسجيل المهام من موقعه.</span><span class="sxs-lookup"><span data-stu-id="995a0-110">Open the task recording from its location.</span></span> <span data-ttu-id="995a0-111">حدد **‬‏‫فتح من هذا الكمبيوتر الشخصي‬‏‫** أو **افتح من Lifecycle Services** ثم حدد **إغلاق** .</span><span class="sxs-lookup"><span data-stu-id="995a0-111">Select **Open from this PC** or **Open from Lifecycle Services** , and then select **Close** .</span></span>
3. <span data-ttu-id="995a0-112">سيؤدي ذلك إلى فتح صفحة **تفاصيل عناصر قائمة الأمان** التي تسرد كائنات الأمان المطلوبة للعملية.</span><span class="sxs-lookup"><span data-stu-id="995a0-112">This will open the **Security menu item details** page that lists the security objects required for the process.</span></span>

 > [!NOTE]
 > <span data-ttu-id="995a0-113">عناصر قائمة **الإجراءات** و **الإخراج** غير مضمّنة في القائمة.</span><span class="sxs-lookup"><span data-stu-id="995a0-113">The **Action** and **Output** menu items are not included in the list.</span></span>

4. <span data-ttu-id="995a0-114">في حقل **‏‫معرف المستخدم** حدد مستخدم.</span><span class="sxs-lookup"><span data-stu-id="995a0-114">In the **User ID** field, select a user.</span></span> <span data-ttu-id="995a0-115">إذا لم يكن لدي المستخدم أذونات لبعض عناصر القائمة، فسيتم تحديث حقل **الأذونات المفقودة** إلى **نعم** .</span><span class="sxs-lookup"><span data-stu-id="995a0-115">If the user does not have permissions for some menu items, the **Missing permissions** field will update to **Yes** .</span></span>
  
  ![صفحة تفاصيل عنصر قائمة الأمان](../media/Security-Menu-Item-Details.png)

5. <span data-ttu-id="995a0-117">حدد **إضافة مرجع** لعرض قائمة بكائنات الأمان، بما في ذلك الأدوار والمهام والامتيازات التي تمنح الاذن المفقود.</span><span class="sxs-lookup"><span data-stu-id="995a0-117">Select **Add Reference** to see a list of the security objects, including roles, duties, and privileges that grant the missing permission.</span></span>
6. <span data-ttu-id="995a0-118">حدد كائن أمان من القائمة:</span><span class="sxs-lookup"><span data-stu-id="995a0-118">Select a security object from the list:</span></span>

    - <span data-ttu-id="995a0-119">في حالة تحديد **الدور** حدد **إضافة دور إلى المستخدم** .</span><span class="sxs-lookup"><span data-stu-id="995a0-119">If **Role** is selected, select **Add role to user** .</span></span> <span data-ttu-id="995a0-120">سيؤدي ذلك إلى فتح صفحة **تعيين مستخدمين إلى أدوار** .</span><span class="sxs-lookup"><span data-stu-id="995a0-120">This will open the **Assign users to roles** page.</span></span> <span data-ttu-id="995a0-121">لمزيد من المعلومات، راجع [تعيين مستخدمين إلى أدوار أمان‬](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="995a0-121">For more information, see [Assign users to security roles](assign-users-security-roles.md) page.</span></span>
    - <span data-ttu-id="995a0-122">في حالة تحديد **الرسوم** فحدد **إضافة رسوم إلى الدور** ، وحدد الأدوار التي يجب إضافه الرسوم إليها، ثم حدد **موافق** .</span><span class="sxs-lookup"><span data-stu-id="995a0-122">If **Duty** is selected, select **Add duty to role** , select the roles that the duty should be added to, and then select **OK** .</span></span>
    - <span data-ttu-id="995a0-123">في حالة تحديد **الامتياز** فحدد **إضافة امتياز إلى الرسوم** ، وحدد الأدوار التي يجب إضافه الرسوم إليها، ثم حدد **موافق** .</span><span class="sxs-lookup"><span data-stu-id="995a0-123">If **Privilege** is selected, select **Add privilege to duties** , select the roles that the duty should be added to, and then select **OK** .</span></span>