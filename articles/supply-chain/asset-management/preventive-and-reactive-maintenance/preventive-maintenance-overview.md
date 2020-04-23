---
title: نظرة عامة على الصيانة الوقائية
description: يشرح هذا الموضوع الصيانة الوقائية في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8949f9b26917c4a93faa5aea74faa0b6735d770f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206002"
---
# <a name="preventive-maintenance-overview"></a><span data-ttu-id="39be4-103">نظرة عامة على الصيانة الوقائية</span><span class="sxs-lookup"><span data-stu-id="39be4-103">Preventive maintenance overview</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="39be4-104">يشرح هذا الموضوع الصيانة الوقائية في إدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="39be4-104">This topic explains preventive maintenance in Asset Management.</span></span> <span data-ttu-id="39be4-105">الصيانة الوقائية هي نظام يتضمن مهام الصيانة المخططة، على سبيل المثال، الخدمة العادية والمعايرة وعمليات الفحص.</span><span class="sxs-lookup"><span data-stu-id="39be4-105">Preventive maintenance is a discipline involving planned maintenance jobs, for example, regular service, calibration, and inspections.</span></span> <span data-ttu-id="39be4-106">في **إدارة الأصول**، يمكنك إنشاء خطط صيانة وإعدادها على الأصول ومواقع العمل.</span><span class="sxs-lookup"><span data-stu-id="39be4-106">In **Asset Management**, you can create maintenance plans and set them up on assets and functional locations.</span></span> <span data-ttu-id="39be4-107">يمكنك أيضًا إعداد دورات الصيانة على مواقع العمل.</span><span class="sxs-lookup"><span data-stu-id="39be4-107">You can also set up maintenance rounds on functional locations.</span></span> <span data-ttu-id="39be4-108">تعتبر خطط الصيانة على الأصول نشطة بغض النظر عن مكان تثبيت الأصل.</span><span class="sxs-lookup"><span data-stu-id="39be4-108">Maintenance plans on assets are active regardless of where the asset is installed.</span></span> <span data-ttu-id="39be4-109">وتعتبر خطط الصيانة ودورات الصيانة في موقع العمل نشطة للأصول المثبتة حاليًا في الموقع.</span><span class="sxs-lookup"><span data-stu-id="39be4-109">Maintenance plans and maintenance rounds on functional location are active for the assets currently installed at the location.</span></span> <span data-ttu-id="39be4-110">بدلاً من إعداد خطط الصيانة على الأصول، أو إعداد دورات الصيانة على مواقع العمل، يمكنك إنشاء دورات صيانة تتضمن أصولاً متعددة يجب أن تنفذ عليها أنواعًا ذات صلة من مهام الصيانة في روتين العمل نفسه.</span><span class="sxs-lookup"><span data-stu-id="39be4-110">Instead of setting up maintenance plans on assets, or setting up maintenance rounds on functional locations, you can create maintenance rounds that include multiple assets on which you need to perform related types of maintenance jobs in the same work routine.</span></span> <span data-ttu-id="39be4-111">تعني دورات الصيانة المنشأة من أصول - بدلاً من إنشائها على مواقع عمل - أنه يمكنك تحديد عدد من الأصول على دورة صيانة واحدة، لم يتم تثبيتها في موقع العمل نفسه.</span><span class="sxs-lookup"><span data-stu-id="39be4-111">Maintenance rounds created from assets - instead of created on functional locations - means that you can select a number of assets for one maintenance round, which are not installed on the same functional location.</span></span>

<span data-ttu-id="39be4-112">تستخدم خطط الصيانة للصيانة الوقائية والتفاعلية‬ على أصول فردية.</span><span class="sxs-lookup"><span data-stu-id="39be4-112">Maintenance plans are used for preventive and reactive maintenance on individual assets.</span></span> <span data-ttu-id="39be4-113">تُستخدم دورات الصيانة للصيانة الوقائية على مجموعة أو مجموعة من الأصول.</span><span class="sxs-lookup"><span data-stu-id="39be4-113">Maintenance rounds are used for preventive maintenance on a group or a set of assets.</span></span> <span data-ttu-id="39be4-114">تُستخدم خطط الصيانة ودورات الصيانة لإنشاء مقترحات أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="39be4-114">Maintenance plans and maintenance rounds are used for generating work order proposals.</span></span> <span data-ttu-id="39be4-115">ويتم حفظ مقترحات أمر العمل كبنود جدول صيانة، يمكن تجميعها وتحويلها إلى أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="39be4-115">The work order proposals are saved as maintenance schedule lines, which can be bundled and converted into work orders.</span></span>

<span data-ttu-id="39be4-116">يوفر الرسم التوضيحي التالي نظرة عامة حول سير العمل من إنشاء خطط الصيانة ودورات الصيانة لإنشاء أوامر العمل للأصول، وذلك استنادًا إلى خطط الصيانة ودورات الصيانة.</span><span class="sxs-lookup"><span data-stu-id="39be4-116">The following illustration provides an overview of the work flow from creating maintenance plans and maintenance rounds to creating work orders for assets, based on those maintenance plans and maintenance rounds.</span></span>

![الشكل 1](media/01-preventive-maintenance.png)

